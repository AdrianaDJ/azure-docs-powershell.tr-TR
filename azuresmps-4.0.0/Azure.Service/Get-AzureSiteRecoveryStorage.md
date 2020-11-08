---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 78DE0AD2-6210-4604-89A8-41915D58BD68
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3c40cb0fd38953ff46fa1138dc91f0b9e97ece75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105576"
---
# <span data-ttu-id="7bb64-101">Get-AzureSiteRecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="7bb64-101">Get-AzureSiteRecoveryStorage</span></span>

## <span data-ttu-id="7bb64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bb64-102">SYNOPSIS</span></span>
<span data-ttu-id="7bb64-103">Kasaya yönelik site kurtarma depolarını alır.</span><span class="sxs-lookup"><span data-stu-id="7bb64-103">Gets Site Recovery Storages for a vault.</span></span>

## <span data-ttu-id="7bb64-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7bb64-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryStorage -Server <ASRServer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7bb64-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7bb64-105">DESCRIPTION</span></span>
<span data-ttu-id="7bb64-106">**Get-AzureSiteRecoveryStorage** cmdlet 'ı geçerli Azure Site Recovery Kasası Için Azure Site Recovery depolarını alır.</span><span class="sxs-lookup"><span data-stu-id="7bb64-106">The **Get-AzureSiteRecoveryStorage** cmdlet gets Azure Site Recovery Storages for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="7bb64-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7bb64-107">EXAMPLES</span></span>

### <span data-ttu-id="7bb64-108">Örnek 1: site kurtarma depolamasını alma</span><span class="sxs-lookup"><span data-stu-id="7bb64-108">Example 1: Get site recovery storage</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryStorage -Server $Servers[0]
Name           : phase2PrimaryStorageClassification
ID             : 1c1d0c0b-0c50-4675-af1a-1fdac70dbb6d
FabricObjectID : 1c1d0c0b-0c50-4675-af1a-1fdac70dbb6d
ServerId       : 774859b0-1966-48cc-9df7-759c441b7a8c
Type           : Classification
FabricType     : VMM

Name           : phase2RecoveryStorageClassification
ID             : 20cf8d92-fd5d-4872-985a-0f4562b8a0bf
FabricObjectID : 20cf8d92-fd5d-4872-985a-0f4562b8a0bf
ServerId       : 774859b0-1966-48cc-9df7-759c441b7a8c
Type           : Classification
FabricType     : VMM
```

<span data-ttu-id="7bb64-109">İlk komut cmdlet 'i **Get-AzureSiteRecoveryServer** cmdlet 'ini kullanarak geçerli Azure Site Recovery Kasası için sunucuları alır.</span><span class="sxs-lookup"><span data-stu-id="7bb64-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="7bb64-110">Komut, $Servers dizi değişkeninde site kurtarma sunucularını depolar.</span><span class="sxs-lookup"><span data-stu-id="7bb64-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="7bb64-111">İkinci komut, $Servers dizisindeki ilk sunucunun site kurtarma depolamasını alır.</span><span class="sxs-lookup"><span data-stu-id="7bb64-111">The second command gets the site recovery storage for the first server in the $Servers array.</span></span>

## <span data-ttu-id="7bb64-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7bb64-112">PARAMETERS</span></span>

### <span data-ttu-id="7bb64-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="7bb64-113">-Profile</span></span>
<span data-ttu-id="7bb64-114">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7bb64-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7bb64-115">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="7bb64-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7bb64-116">-Sunucu</span><span class="sxs-lookup"><span data-stu-id="7bb64-116">-Server</span></span>
<span data-ttu-id="7bb64-117">Azure Site Recovery depolama sunucusu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7bb64-117">Specifies a server for Azure Site Recovery Storage.</span></span>
<span data-ttu-id="7bb64-118">Bir **Asrserver** nesnesi edinmek için **Get-AzureSiteRecoveryServer** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7bb64-118">To obtain an **ASRServer** object, use the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>

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

### <span data-ttu-id="7bb64-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bb64-119">CommonParameters</span></span>
<span data-ttu-id="7bb64-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7bb64-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bb64-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bb64-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bb64-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7bb64-122">INPUTS</span></span>

## <span data-ttu-id="7bb64-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7bb64-123">OUTPUTS</span></span>

## <span data-ttu-id="7bb64-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7bb64-124">NOTES</span></span>

## <span data-ttu-id="7bb64-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7bb64-125">RELATED LINKS</span></span>

[<span data-ttu-id="7bb64-126">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="7bb64-126">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)


