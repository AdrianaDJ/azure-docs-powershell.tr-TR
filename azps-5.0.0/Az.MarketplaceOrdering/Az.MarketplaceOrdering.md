---
Module Name: Az.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
ms.openlocfilehash: dfcfd580312209bfdb0c197b95c2f655b9ac0723
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278893"
---
# <span data-ttu-id="17e8e-101">Az. Pazar Placesıralanırken modül</span><span class="sxs-lookup"><span data-stu-id="17e8e-101">Az.MarketplaceOrdering Module</span></span>
## <span data-ttu-id="17e8e-102">Tanım</span><span class="sxs-lookup"><span data-stu-id="17e8e-102">Description</span></span>
<span data-ttu-id="17e8e-103">Bu bölümdeki konular, Azure Resource Manager (ARM) çerçevesindeki Azure</span><span class="sxs-lookup"><span data-stu-id="17e8e-103">The topics in this section document the Azure PowerShell cmdlets for Azure MarketplaceOrdering in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="17e8e-104">Cmdlet 'ler Microsoft. Azure. Commands. Marketplacesıralanırken ad alanında bulunur.</span><span class="sxs-lookup"><span data-stu-id="17e8e-104">The cmdlets exist in the Microsoft.Azure.Commands.MarketplaceOrdering namespace.</span></span> <span data-ttu-id="17e8e-105">Bu cmdlet 'ler, Azure kullanıcılarının bu çözümler için programlı dağıtıma olanak sağlayan bir Pazaryeri yasal koşullarını kabul etmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="17e8e-105">These cmdlets allow azure users to accept the legal terms for a marketplace offering further allowing programmatic deployment for these solutions.</span></span> <span data-ttu-id="17e8e-106">Kullanıcılar halen kabul edilmiş yasal şartlar kümesini de reddedebilir.</span><span class="sxs-lookup"><span data-stu-id="17e8e-106">Users may also reject set of legal terms already accepted.</span></span>

## <span data-ttu-id="17e8e-107">Az. Pazar Placesıralanırken cmdlet 'Ler</span><span class="sxs-lookup"><span data-stu-id="17e8e-107">Az.MarketplaceOrdering Cmdlets</span></span>
### [<span data-ttu-id="17e8e-108">Get-Azpazar Placeterms</span><span class="sxs-lookup"><span data-stu-id="17e8e-108">Get-AzMarketplaceTerms</span></span>](Get-AzMarketplaceTerms.md)
<span data-ttu-id="17e8e-109">Belirli bir yayıncı kimliği (yayımcı), teklif kimliği (ürün) ve plan kimliği (adı) için anlaşma şartlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="17e8e-109">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="17e8e-110">Bu komut tarafından döndürülen terimler nesnesinin yasal şartları kabul etmesi için Set-AzMarketplaceTerms geçirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="17e8e-110">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

### [<span data-ttu-id="17e8e-111">Set-Azpazar Placeterms</span><span class="sxs-lookup"><span data-stu-id="17e8e-111">Set-AzMarketplaceTerms</span></span>](Set-AzMarketplaceTerms.md)
<span data-ttu-id="17e8e-112">Verilen Yayımcı kimliği (yayımcı), teklif kimliği (ürün) ve plan kimliği (adı) için koşulları kabul edin veya reddedin.</span><span class="sxs-lookup"><span data-stu-id="17e8e-112">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="17e8e-113">Sözleşme şartlarını almak için lütfen Get-AzMarketplaceTerms kullanın.</span><span class="sxs-lookup"><span data-stu-id="17e8e-113">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

