<template>
  <button type="button" class="mct-button">
    <span class="icon-text-container" style="display: flex; align-items: center;">
      <svg-icon :type="iconType" :path="iconPath" class="mct-button-icon"></svg-icon>
      <span>{{ label }}</span>
    </span>
  </button>
</template>

<script>
import SvgIcon from '@jamescoyle/vue-icon';
import * as mdiIcons from '@mdi/js';

export default {
  name: 'MctButton',
  components: {
    SvgIcon
  },
  props: {
    iconType: {
      type: String,
      default: 'mdi'
    },
    iconName: {
      type: String,
      required: true
    },
    label: {
      type: String,
      required: true
    }
  },
  computed: {
    iconPath() {
      return mdiIcons[this.iconName];
    }
  }
}
</script>

<style scoped>
.mct-button {
  border: none;
  color: white;
  padding: 5px 10px;
  border-radius: 9px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 18px;
  transition: background-color 0.2s, transform 0.05s, box-shadow 0.1s;
  z-index: 55;
}

.mct-button:active {
  transform: scale(0.95);

}

.mct-button {
  border-radius: 9px;
  font-size: 16px;
  transition: background-color 0.2s, transform 0.05s, box-shadow 0.1s, border 0.2s;
  outline: none;
}

.mct-button-icon {
  margin-right: 7px;
  height: 16px !important;
  width: 16px !important;
}

/* primary */
.mct-button-primary {
  background-color: var(--primary);
  box-shadow: 0px 0px 10px hsl(var(--primary-h), var(--primary-s), calc(var(--primary-l) - 3%));
}

.mct-button-primary:hover {
  box-shadow: 0px 0px 10px hsl(var(--primary-h), var(--primary-s), calc(var(--primary-l) + 3%));
  background-color: hsl(var(--primary-h), var(--primary-s), calc(var(--primary-l) + 3%));
}

.mct-button-primary:active {
  box-shadow: 0px 0px 10px hsl(var(--primary-h), var(--primary-s), calc(var(--primary-l) - 3%));
  background-color: hsl(var(--primary-h), var(--primary-s), calc(var(--primary-l) - 3%));
}

/* danger */
.mct-button-danger {
  background-color: var(--danger);
  box-shadow: 0px 0px 10px hsl(var(--danger-h), var(--danger-s), calc(var(--danger-l) - 3%));

}

.mct-button-danger:hover {
  box-shadow: 0px 0px 10px hsl(var(--danger-h), var(--danger-s), calc(var(--danger-l) + 3%));
  background-color: hsl(var(--danger-h), var(--danger-s), calc(var(--danger-l) + 3%));
}

.mct-button-danger:active {
  box-shadow: 0px 0px 10px hsl(var(--danger-h), var(--danger-s), calc(var(--danger-l) - 3%));
  background-color: hsl(var(--danger-h), var(--danger-s), calc(var(--danger-l) - 3%));
}

/* warning */
.mct-button-warning {
  background-color: var(--warning);
  box-shadow: 0px 0px 10px hsl(var(--warning-h), var(--warning-s), calc(var(--warning-l) - 3%));

}

.mct-button-warning:hover {
  box-shadow: 0px 0px 10px hsl(var(--warning-h), var(--warning-s), calc(var(--warning-l) + 3%));
  background-color: hsl(var(--warning-h), var(--warning-s), calc(var(--warning-l) + 3%));
}

.mct-button-warning:active {
  box-shadow: 0px 0px 10px hsl(var(--warning-h), var(--warning-s), calc(var(--warning-l) - 3%));
  background-color: hsl(var(--warning-h), var(--warning-s), calc(var(--warning-l) - 3%));
}

/* success */
.mct-button-success {
  background-color: var(--success);
  box-shadow: 0px 0px 10px hsl(var(--success-h), var(--success-s), calc(var(--success-l) - 3%));

}

.mct-button-success:hover {
  box-shadow: 0px 0px 10px hsl(var(--success-h), var(--success-s), calc(var(--success-l) + 3%));
  background-color: hsl(var(--success-h), var(--success-s), calc(var(--success-l) + 3%));
}

.mct-button-success:active {
  box-shadow: 0px 0px 10px hsl(var(--success-h), var(--success-s), calc(var(--success-l) - 3%));
  background-color: hsl(var(--success-h), var(--success-s), calc(var(--success-l) - 3%));
}
</style>
