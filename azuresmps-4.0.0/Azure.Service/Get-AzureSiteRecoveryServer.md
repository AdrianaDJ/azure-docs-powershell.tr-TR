---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 3EC274C9-9BF6-4B39-BC70-C7F9D780805D
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4081d6d072aadd6a4ae7d09ff57748a8f2cb697
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105580"
---
# <span data-ttu-id="939a2-101">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="939a2-101">Get-AzureSiteRecoveryServer</span></span>

## <span data-ttu-id="939a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="939a2-102">SYNOPSIS</span></span>
<span data-ttu-id="939a2-103">Site kurtarma sunucularını bir site kurtarma Kasası 'na getirir.</span><span class="sxs-lookup"><span data-stu-id="939a2-103">Gets Site Recovery servers registered a Site Recovery vault.</span></span>

## <span data-ttu-id="939a2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="939a2-104">SYNTAX</span></span>

### <span data-ttu-id="939a2-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="939a2-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryServer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="939a2-106">Byıd</span><span class="sxs-lookup"><span data-stu-id="939a2-106">ById</span></span>
```
Get-AzureSiteRecoveryServer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="939a2-107">ByName</span><span class="sxs-lookup"><span data-stu-id="939a2-107">ByName</span></span>
```
Get-AzureSiteRecoveryServer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="939a2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="939a2-108">DESCRIPTION</span></span>
<span data-ttu-id="939a2-109">**Get-AzureSiteRecoveryServer** cmdlet 'i, geçerli site kurtarma kasasına kaydedilen Azure Site Recovery sunucuları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="939a2-109">The **Get-AzureSiteRecoveryServer** cmdlet gets information about Azure Site Recovery servers registered to the current Site Recovery vault.</span></span>

## <span data-ttu-id="939a2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="939a2-110">EXAMPLES</span></span>

### <span data-ttu-id="939a2-111">Örnek 1: site kurtarma sunucusu hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="939a2-111">Example 1: Get information about a Site Recovery server</span></span>
```
PS C:\> Get-AzureSiteRecoveryServer
ID              : cd7dec80-1144-4531-9ab3-888b8ab39bee
Name            : server1.contoso.com
LastHeartbeat   : 9/23/2014 3:51:22 PM
ProviderVersion : 3.5.520.0
ServerVersion   : 3.2.7634.0

ID              : f5e713fe-5b6d-4641-9690-6fe74c976b8e
Name            : Server2.contoso.com
LastHeartbeat   : 8/13/2014 2:28:58 PM
ProviderVersion : 3.5
ServerVersion   : 3.2.7510.0
```

<span data-ttu-id="939a2-112">Bu komut, bir Azure Site Recovery sunucusu hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="939a2-112">This command gets information about an Azure Site Recovery server.</span></span>

## <span data-ttu-id="939a2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="939a2-113">PARAMETERS</span></span>

### <span data-ttu-id="939a2-114">-ID</span><span class="sxs-lookup"><span data-stu-id="939a2-114">-Id</span></span>
<span data-ttu-id="939a2-115">Sunucunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="939a2-115">Specifies the ID of a server.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="939a2-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="939a2-116">-Name</span></span>
<span data-ttu-id="939a2-117">Sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="939a2-117">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="939a2-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="939a2-118">-Profile</span></span>
<span data-ttu-id="939a2-119">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="939a2-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="939a2-120">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="939a2-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="939a2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="939a2-121">CommonParameters</span></span>
<span data-ttu-id="939a2-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="939a2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="939a2-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="939a2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="939a2-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="939a2-124">INPUTS</span></span>

## <span data-ttu-id="939a2-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="939a2-125">OUTPUTS</span></span>

## <span data-ttu-id="939a2-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="939a2-126">NOTES</span></span>

## <span data-ttu-id="939a2-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="939a2-127">RELATED LINKS</span></span>

[<span data-ttu-id="939a2-128">Azure Site Recovery Hizmetleri cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="939a2-128">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


