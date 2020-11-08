---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 615D2C5D-AB31-45DB-9535-9B9C8E957322
online version: ''
schema: 2.0.0
ms.openlocfilehash: 96b51b49d76093be96eeab26417f4a70f70c4627
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105592"
---
# <span data-ttu-id="27469-101">Get-AzureSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="27469-101">Get-AzureSiteRecoveryNetwork</span></span>

## <span data-ttu-id="27469-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27469-102">SYNOPSIS</span></span>
<span data-ttu-id="27469-103">Geçerli kasa için site kurtarma tarafından yönetilen ağlar hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="27469-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="27469-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="27469-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryNetwork -Server <ASRServer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="27469-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="27469-105">DESCRIPTION</span></span>
<span data-ttu-id="27469-106">**Get-AzureSiteRecoveryNetwork** cmdlet 'i, geçerli site kurtarma Kasası Için Azure Site Recovery ağları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="27469-106">The **Get-AzureSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Site Recovery vault.</span></span>

## <span data-ttu-id="27469-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="27469-107">EXAMPLES</span></span>

### <span data-ttu-id="27469-108">Örnek 1: site kurtarma ağlarını alma</span><span class="sxs-lookup"><span data-stu-id="27469-108">Example 1: Get site recovery networks</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetwork -Server $Servers[0]
Name                : phase2RecoveryVMNetwork
ID                  : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
FabricObjectID      : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
ServerId            : 774859b0-1966-48cc-9df7-759c441b7a8c
Type                : NoIsolation
FabricType          : VMM
VmNetworkSubnetList : {}

Name                : phase2PrimaryVMNetwork
ID                  : d903e2c6-3141-4cef-bfe1-04616cd43cbb
FabricObjectID      : d903e2c6-3141-4cef-bfe1-04616cd43cbb
ServerId            : 774859b0-1966-48cc-9df7-759c441b7a8c
Type                : NoIsolation
FabricType          : VMM
VmNetworkSubnetList : {}
```

<span data-ttu-id="27469-109">İlk komut cmdlet 'i **Get-AzureSiteRecoveryServer** cmdlet 'ini kullanarak geçerli Azure Site Recovery Kasası için sunucuları alır.</span><span class="sxs-lookup"><span data-stu-id="27469-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="27469-110">Komut, $Servers dizi değişkeninde site kurtarma sunucularını depolar.</span><span class="sxs-lookup"><span data-stu-id="27469-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="27469-111">İkinci komut, $Servers dizisindeki ilk sunucu için site kurtarma ağını alır.</span><span class="sxs-lookup"><span data-stu-id="27469-111">The second command gets the site recovery network for the first server in the $Servers array.</span></span>

## <span data-ttu-id="27469-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="27469-112">PARAMETERS</span></span>

### <span data-ttu-id="27469-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="27469-113">-Profile</span></span>
<span data-ttu-id="27469-114">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="27469-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="27469-115">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="27469-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="27469-116">-Sunucu</span><span class="sxs-lookup"><span data-stu-id="27469-116">-Server</span></span>
<span data-ttu-id="27469-117">Site kurtarma sunucusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="27469-117">Specifies a Site Recovery server.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27469-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27469-118">CommonParameters</span></span>
<span data-ttu-id="27469-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="27469-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27469-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27469-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27469-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="27469-121">INPUTS</span></span>

## <span data-ttu-id="27469-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="27469-122">OUTPUTS</span></span>

## <span data-ttu-id="27469-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="27469-123">NOTES</span></span>

## <span data-ttu-id="27469-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="27469-124">RELATED LINKS</span></span>

[<span data-ttu-id="27469-125">Azure Site Recovery Hizmetleri cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="27469-125">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


