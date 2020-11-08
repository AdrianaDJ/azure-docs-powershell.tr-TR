---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 4F083EBC-7D7E-4836-8AAB-6BF2B08162DF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6a69d54b315319e3dacc150edc2a8737be9b96e3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105575"
---
# <span data-ttu-id="beb1d-101">Get-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="beb1d-101">Get-AzureSiteRecoveryStorageMapping</span></span>

## <span data-ttu-id="beb1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="beb1d-102">SYNOPSIS</span></span>
<span data-ttu-id="beb1d-103">Kasa için site kurtarma depolama nesnelerinin eşleştirmelerini alır.</span><span class="sxs-lookup"><span data-stu-id="beb1d-103">Gets mappings of Site Recovery Storage objects for a vault.</span></span>

## <span data-ttu-id="beb1d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="beb1d-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryStorageMapping -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="beb1d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="beb1d-105">DESCRIPTION</span></span>
<span data-ttu-id="beb1d-106">**Get-AzureSiteRecoveryStorageMapping** cmdlet 'i, geçerli Azure Site Recovery Kasası Için Azure Site Recovery depolama nesnelerinin eşlemelerini alır.</span><span class="sxs-lookup"><span data-stu-id="beb1d-106">The **Get-AzureSiteRecoveryStorageMapping** cmdlet gets mappings of Azure Site Recovery Storage objects for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="beb1d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="beb1d-107">EXAMPLES</span></span>

### <span data-ttu-id="beb1d-108">Örnek 1: depolama nesnesiyle kurtarma depolama nesnesi arasındaki eşlemeyi alma</span><span class="sxs-lookup"><span data-stu-id="beb1d-108">Example 1: Get the mapping between a Storage object and a recovery Storage object</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryStorageMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[1]
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryStorageId    : 1c1d0c0b-0c50-4675-af1a-1fdac70dbb6d
PrimaryStorageName  : phase2PrimaryStorageClassification
RecoveryServerId    : 774859b0-1966-48cc-9df7-759c441b7a8c
RecoveryStorageId   : 20cf8d92-fd5d-4872-985a-0f4562b8a0bf
RecoveryStorageName : phase2RecoveryStorageClassification
```

<span data-ttu-id="beb1d-109">İlk komut cmdlet 'i **Get-AzureSiteRecoveryServer** cmdlet 'ini kullanarak geçerli Azure Site Recovery Kasası için sunucuları alır.</span><span class="sxs-lookup"><span data-stu-id="beb1d-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="beb1d-110">Komut, $Servers dizi değişkeninde site kurtarma sunucularını depolar.</span><span class="sxs-lookup"><span data-stu-id="beb1d-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="beb1d-111">İkinci komut iki Azure depolama nesnesi arasındaki eşlemeyi alır.</span><span class="sxs-lookup"><span data-stu-id="beb1d-111">The second command gets the mapping between two Azure Storage objects.</span></span>
<span data-ttu-id="beb1d-112">Komut, $Servers ilk öğesi olarak depolama nesnesi eşlemesi için birincil sunucuyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="beb1d-112">The command specifies the primary server for the Storage object mapping as the first element of $Servers.</span></span>
<span data-ttu-id="beb1d-113">Komut, kurtarma depolama nesnesinin sunucusunu $Servers ikinci öğesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="beb1d-113">The command specifies the server for the recovery Storage object as the second element of $Servers.</span></span>

## <span data-ttu-id="beb1d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="beb1d-114">PARAMETERS</span></span>

### <span data-ttu-id="beb1d-115">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="beb1d-115">-PrimaryServer</span></span>
<span data-ttu-id="beb1d-116">Birincil sunucuyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="beb1d-116">Specifies the primary server.</span></span>
<span data-ttu-id="beb1d-117">Sunucu edinmek için **Get-AzureSiteRecoveryServer** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="beb1d-117">To obtain a server, use the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beb1d-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="beb1d-118">-Profile</span></span>
<span data-ttu-id="beb1d-119">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="beb1d-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="beb1d-120">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="beb1d-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="beb1d-121">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="beb1d-121">-RecoveryServer</span></span>
<span data-ttu-id="beb1d-122">Kurtarma sunucusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="beb1d-122">Specifies the recovery server.</span></span>
<span data-ttu-id="beb1d-123">Sunucu edinmek için **Get-AzureSiteRecoveryServer** kullanın.</span><span class="sxs-lookup"><span data-stu-id="beb1d-123">To obtain a server, use **Get-AzureSiteRecoveryServer**.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beb1d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beb1d-124">CommonParameters</span></span>
<span data-ttu-id="beb1d-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="beb1d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beb1d-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="beb1d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beb1d-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="beb1d-127">INPUTS</span></span>

## <span data-ttu-id="beb1d-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="beb1d-128">OUTPUTS</span></span>

## <span data-ttu-id="beb1d-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="beb1d-129">NOTES</span></span>

## <span data-ttu-id="beb1d-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="beb1d-130">RELATED LINKS</span></span>

[<span data-ttu-id="beb1d-131">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="beb1d-131">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)

[<span data-ttu-id="beb1d-132">New-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="beb1d-132">New-AzureSiteRecoveryStorageMapping</span></span>](./New-AzureSiteRecoveryStorageMapping.md)

[<span data-ttu-id="beb1d-133">Remove-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="beb1d-133">Remove-AzureSiteRecoveryStorageMapping</span></span>](./Remove-AzureSiteRecoveryStorageMapping.md)


