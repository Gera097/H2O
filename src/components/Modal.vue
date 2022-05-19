<script setup>
const props = defineProps({
  show: Boolean
})
</script>

<template>
  <Transition name="modal">
    <div v-if="show" class="modal-mask" @click="$emit('close')">
        <div class="modal-container" @click.stop>     
            <button class="modal-default-button" @click="$emit('close')">
            <i class="fi fi-br-cross"></i>
            </button>
            <div class="modal-body">
            <slot name="body">default body</slot>
            </div>
        </div>
    </div>
  </Transition>
</template>

<style scoped>
.modal-mask {
  position: fixed;
  z-index: 9998;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.1);
  transition: opacity 0.3s ease;
}

.modal-container {
  width: 80%;
  margin: 5em auto;
  padding: 1em;
  background-color: rgba(255, 255, 255, 0.185);
  border-radius: 1em;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.33);
  transition: all 0.3s ease;
}

.modal-body {
    max-height: calc(70vh);
    overflow: auto;
}
.modal-default-button {
    background-color: #023d8a00;
    color: #023E8A;
    border: 0px;
}

/*
 * The following styles are auto-applied to elements with
 * transition="modal" when their visibility is toggled
 * by Vue.js.
 *
 * You can easily play with the modal transition by editing
 * these styles.
 */

.modal-enter-from {
  opacity: 0;
}

.modal-leave-to {
  opacity: 0;
}

.modal-enter-from .modal-container,
.modal-leave-to .modal-container {
  -webkit-transform: scale(1.1);
  transform: scale(1.1);
}
</style>