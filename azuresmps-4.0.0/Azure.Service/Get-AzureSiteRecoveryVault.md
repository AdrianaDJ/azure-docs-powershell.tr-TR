---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2A6DDF5F-2906-4DB5-B791-B6BF590261A0
online version: ''
schema: 2.0.0
ms.openlocfilehash: ffdf63e9e4d1d8e34dc63cb90c1fa0de15369fbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106565"
---
# <span data-ttu-id="6495e-101">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="6495e-101">Get-AzureSiteRecoveryVault</span></span>

## <span data-ttu-id="6495e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6495e-102">SYNOPSIS</span></span>
<span data-ttu-id="6495e-103">Geçerli aboneliğin site kurtarma şaşırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="6495e-103">Gets Site Recovery vaults from the current subscription.</span></span>

## <span data-ttu-id="6495e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6495e-104">SYNTAX</span></span>

### <span data-ttu-id="6495e-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6495e-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryVault [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6495e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6495e-106">ByName</span></span>
```
Get-AzureSiteRecoveryVault -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6495e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6495e-107">DESCRIPTION</span></span>
<span data-ttu-id="6495e-108">**Get-AzureSiteRecoveryVault** cmdlet 'i, geçerli abonelikteki Azure Site Recovery Kasası veya belirli bir site kurtarma Kasası listesini alır.</span><span class="sxs-lookup"><span data-stu-id="6495e-108">The **Get-AzureSiteRecoveryVault** cmdlet gets a list of Azure Site Recovery vaults or a specific Site Recovery vault from the current subscription.</span></span>

## <span data-ttu-id="6495e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6495e-109">EXAMPLES</span></span>

### <span data-ttu-id="6495e-110">Örnek 1: etkin kasayı alma</span><span class="sxs-lookup"><span data-stu-id="6495e-110">Example 1: Get the active vault</span></span>
```
PS C:\> Get-AzureSiteRecoveryVault
Name             : ContosoVault
ID               : 6467459117394545458
CloudServiceName : CS-West-US-RecoveryServices
SubscriptionId   : a5aa5997-33e5-46cc-8ab8-b8d89b76b7ba
StatusReason     : 
Status           : Active
Location         : West US
```

<span data-ttu-id="6495e-111">Bu komut, etkin Azure Site kurtarma kasasından alır.</span><span class="sxs-lookup"><span data-stu-id="6495e-111">This command gets the active Azure Site Recovery vault.</span></span>

## <span data-ttu-id="6495e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6495e-112">PARAMETERS</span></span>

### <span data-ttu-id="6495e-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="6495e-113">-Name</span></span>
<span data-ttu-id="6495e-114">Alınacak kasaın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6495e-114">Specifies the name of the vault to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6495e-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="6495e-115">-Profile</span></span>
<span data-ttu-id="6495e-116">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6495e-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6495e-117">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="6495e-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6495e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6495e-118">CommonParameters</span></span>
<span data-ttu-id="6495e-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6495e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6495e-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6495e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6495e-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6495e-121">INPUTS</span></span>

## <span data-ttu-id="6495e-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6495e-122">OUTPUTS</span></span>

## <span data-ttu-id="6495e-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6495e-123">NOTES</span></span>

## <span data-ttu-id="6495e-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6495e-124">RELATED LINKS</span></span>

[<span data-ttu-id="6495e-125">New-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="6495e-125">New-AzureSiteRecoveryVault</span></span>](./New-AzureSiteRecoveryVault.md)


