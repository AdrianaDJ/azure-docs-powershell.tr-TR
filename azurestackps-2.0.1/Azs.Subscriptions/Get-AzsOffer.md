---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/get-azsoffer
schema: 2.0.0
ms.openlocfilehash: 7b2fcb224486915e78bdd90a84941ac0207a45c3
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94105334"
---
# <span data-ttu-id="84ac8-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="84ac8-101">Get-AzsOffer</span></span>

## <span data-ttu-id="84ac8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84ac8-102">SYNOPSIS</span></span>
<span data-ttu-id="84ac8-103">Kök sağlayıcı için genel teklifler listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="84ac8-103">Get the list of public offers for the root provider.</span></span>

## <span data-ttu-id="84ac8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="84ac8-104">SYNTAX</span></span>

```
Get-AzsOffer [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="84ac8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="84ac8-105">DESCRIPTION</span></span>
<span data-ttu-id="84ac8-106">Kök sağlayıcı için genel teklifler listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="84ac8-106">Get the list of public offers for the root provider.</span></span>

## <span data-ttu-id="84ac8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="84ac8-107">EXAMPLES</span></span>

### <span data-ttu-id="84ac8-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="84ac8-108">Example 1</span></span>
```powershell
PS C:\> Get-AzsOffer | fl *

Description : 
DisplayName : TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6
Id          : /delegatedProviders/default/offers/TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6
Name        : TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6

Description : 
DisplayName : TestOffer-8322dc27-47a0-4446-89a0-eb5a0ec3b12b
Id          : /delegatedProviders/default/offers/TestOffer-8322dc27-47a0-4446-89a0-eb5a0ec3b12b
Name        : TestOffer-8322dc27-47a0-4446-89a0-eb5a0ec3b12b
```

<span data-ttu-id="84ac8-109">Genel teklifler listesini alma</span><span class="sxs-lookup"><span data-stu-id="84ac8-109">Get the list of public offers</span></span>

## <span data-ttu-id="84ac8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="84ac8-110">PARAMETERS</span></span>

### <span data-ttu-id="84ac8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84ac8-111">-DefaultProfile</span></span>
<span data-ttu-id="84ac8-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="84ac8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="84ac8-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84ac8-113">CommonParameters</span></span>
<span data-ttu-id="84ac8-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="84ac8-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84ac8-115">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="84ac8-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84ac8-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="84ac8-116">INPUTS</span></span>

## <span data-ttu-id="84ac8-117">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="84ac8-117">OUTPUTS</span></span>

### <span data-ttu-id="84ac8-118">Microsoft. Azure. PowerShell. cmdlet. Subscription. modeller. Api20151101. ıteklifini</span><span class="sxs-lookup"><span data-stu-id="84ac8-118">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.IOffer</span></span>



## <span data-ttu-id="84ac8-119">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="84ac8-119">NOTES</span></span>

## <span data-ttu-id="84ac8-120">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="84ac8-120">RELATED LINKS</span></span>

