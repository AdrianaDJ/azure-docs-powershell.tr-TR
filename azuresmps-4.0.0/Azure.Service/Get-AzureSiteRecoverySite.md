---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 6DD09F28-BFAE-4F9B-BF9C-F09767F9BFEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9151cb5a64b5873ab1c63420a97eb2e7bcffc0ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105577"
---
# <span data-ttu-id="ff1ef-101">Get-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="ff1ef-101">Get-AzureSiteRecoverySite</span></span>

## <span data-ttu-id="ff1ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff1ef-102">SYNOPSIS</span></span>
<span data-ttu-id="ff1ef-103">Bir site kurtarma kasasından Hyper-V sitelerini alır.</span><span class="sxs-lookup"><span data-stu-id="ff1ef-103">Gets the Hyper-V sites from a Site Recovery vault.</span></span>

## <span data-ttu-id="ff1ef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ff1ef-104">SYNTAX</span></span>

```
Get-AzureSiteRecoverySite [-Vault <ASRVault>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ff1ef-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ff1ef-105">DESCRIPTION</span></span>
<span data-ttu-id="ff1ef-106">**Get-AzureSiteRecoverySite** cmdlet 'ı bir Azure Site Recovery kasasındaki Hyper-V sitelerini alır.</span><span class="sxs-lookup"><span data-stu-id="ff1ef-106">The **Get-AzureSiteRecoverySite** cmdlet gets the Hyper-V sites in an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="ff1ef-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ff1ef-107">EXAMPLES</span></span>

### <span data-ttu-id="ff1ef-108">Örnek 1: kurtarma sitelerini alma</span><span class="sxs-lookup"><span data-stu-id="ff1ef-108">Example 1: Get recovery sites</span></span>
```
PS C:\> Get-AzureSiteRecoverySite
Type                                    Name                                    ID
----                                    ----                                    --
HyperVSite                              RecoverySite07                          f16829b4-5b01-4209-a6cf-8e0aff1fe328
```

<span data-ttu-id="ff1ef-109">Bu komut, geçerli kasa için kurtarma sitelerini alır.</span><span class="sxs-lookup"><span data-stu-id="ff1ef-109">This command gets the recovery sites for the current vault.</span></span>

## <span data-ttu-id="ff1ef-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ff1ef-110">PARAMETERS</span></span>

### <span data-ttu-id="ff1ef-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="ff1ef-111">-Profile</span></span>
<span data-ttu-id="ff1ef-112">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ff1ef-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ff1ef-113">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="ff1ef-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ff1ef-114">-Kasa</span><span class="sxs-lookup"><span data-stu-id="ff1ef-114">-Vault</span></span>
<span data-ttu-id="ff1ef-115">Sitelerin alınacağı bir kasa belirtir.</span><span class="sxs-lookup"><span data-stu-id="ff1ef-115">Specifies a vault for which to get sites.</span></span>
<span data-ttu-id="ff1ef-116">Bir **Asrkasa** nesnesi edinmek için **Get-AzureSiteRecoveryVault** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ff1ef-116">To obtain an **ASRVault** object, use the **Get-AzureSiteRecoveryVault** cmdlet.</span></span>

```yaml
Type: ASRVault
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff1ef-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff1ef-117">CommonParameters</span></span>
<span data-ttu-id="ff1ef-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ff1ef-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff1ef-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff1ef-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff1ef-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ff1ef-120">INPUTS</span></span>

## <span data-ttu-id="ff1ef-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ff1ef-121">OUTPUTS</span></span>

## <span data-ttu-id="ff1ef-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ff1ef-122">NOTES</span></span>

## <span data-ttu-id="ff1ef-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ff1ef-123">RELATED LINKS</span></span>

[<span data-ttu-id="ff1ef-124">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="ff1ef-124">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)

[<span data-ttu-id="ff1ef-125">New-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="ff1ef-125">New-AzureSiteRecoverySite</span></span>](./New-AzureSiteRecoverySite.md)


