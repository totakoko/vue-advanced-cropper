<script>
import bem from 'easy-bem';
import draggable from '../../mixins/draggable';
import classnames from 'classnames';

export default {
	name: 'DraggableElement',
	mixins: [draggable],
	props: {
		classname: {
			type: String
		}
	},
};
</script>

<template>
  <div
    ref="draggable"
    :class="classname"
    @touchstart="onTouchStart"
    @mousedown="onMouseDown"
    @mouseover="onMouseOver"
    @mouseleave="onMouseLeave"
  >
    <slot />
  </div>
</template>
