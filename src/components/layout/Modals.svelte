<script>
	import { activeModal } from '@lib/stores'

	import Connect from '../modals/Connect.svelte'
	import ClosePosition from '../modals/ClosePosition.svelte'
	import Deposit from '../modals/Deposit.svelte'
	import Withdraw from '../modals/Withdraw.svelte'
	import MarketInfo from '../modals/MarketInfo.svelte'

</script>

{#if $activeModal && $activeModal.name == 'Connect'}
<Connect />
{/if}

{#if $activeModal && $activeModal.name == 'ClosePosition'}
<ClosePosition data={$activeModal.data} />
{/if}

{#if $activeModal && $activeModal.name == 'Deposit'}
<Deposit />
{/if}

{#if $activeModal && $activeModal.name == 'Withdraw'}
<Withdraw />
{/if}

{#if $activeModal && $activeModal.name == 'MarketInfo'}
<MarketInfo data={$activeModal.data} />
{/if}