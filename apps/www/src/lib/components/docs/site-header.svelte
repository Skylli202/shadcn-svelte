<script lang="ts">
	import {
		Icons,
		ModeToggle,
		MainNav,
		MobileNav,
		CommandMenu
	} from "@/components/docs";
	import { buttonVariants } from "@/registry/new-york/ui/button";
	import { siteConfig } from "$lib/config/site";
	import { cn } from "$lib/utils";
</script>

<header
	class="supports-[backdrop-filter]:bg-background/60 sticky top-0 z-50 w-full border-b bg-background/95 shadow-sm backdrop-blur"
>
	<div class="container flex h-14 items-center">
		<MainNav />
		<MobileNav />
		<div
			class="flex flex-1 items-center justify-between space-x-2 sm:space-x-4 md:justify-end"
		>
			<div class="w-full flex-1 md:w-auto md:flex-none">
				<CommandMenu />
			</div>
			<nav class="flex items-center">
				<a
					href={siteConfig.links.github}
					target="_blank"
					rel="noopener noreferrer"
				>
					<div
						class={cn(
							buttonVariants({
								size: "sm",
								variant: "ghost"
							}),
							"w-9 px-0"
						)}
					>
						<Icons.gitHub class="h-4 w-4" />
						<span class="sr-only">GitHub</span>
					</div>
				</a>
				<a
					href={siteConfig.links.twitter}
					target="_blank"
					rel="noreferrer"
				>
					<div
						class={cn(
							buttonVariants({
								size: "sm",
								variant: "ghost"
							}),
							"w-9 px-0"
						)}
					>
						<Icons.twitter class="h-3 w-3 fill-current" />
						<span class="sr-only"
							>X (formerly known as Twitter)</span
						>
					</div>
				</a>
				<ModeToggle />
			</nav>
		</div>
	</div>
</header>
