---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 6802F2E9-5925-4E92-AEB8-827B5A303617
online version: ''
schema: 2.0.0
ms.openlocfilehash: 153e30c03de7a0a5c404526bd06b9acb2f0678f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106217"
---
# <span data-ttu-id="b19f8-101">New-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="b19f8-101">New-AzureSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="b19f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b19f8-102">SYNOPSIS</span></span>
<span data-ttu-id="b19f8-103">Sanal ağlar arasında eşleme oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b19f8-103">Creates a mapping between virtual networks.</span></span>

## <span data-ttu-id="b19f8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b19f8-104">SYNTAX</span></span>

### <span data-ttu-id="b19f8-105">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="b19f8-105">EnterpriseToEnterprise</span></span>
```
New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork <ASRNetwork> -RecoveryNetwork <ASRNetwork>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b19f8-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="b19f8-106">EnterpriseToAzure</span></span>
```
New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork <ASRNetwork> -AzureSubscriptionId <String>
 -AzureVMNetworkId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b19f8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b19f8-107">DESCRIPTION</span></span>
<span data-ttu-id="b19f8-108">**New-AzureSiteRecoveryNetworkMapping** cmdlet iki sanal ağ arasında bir eşleme oluşturur ve bunu izlemek Için bir Azure Site kurtarma işi döndürür.</span><span class="sxs-lookup"><span data-stu-id="b19f8-108">The **New-AzureSiteRecoveryNetworkMapping** cmdlet creates a mapping between two virtual networks and returns an Azure Site Recovery job to track it.</span></span>

## <span data-ttu-id="b19f8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b19f8-109">EXAMPLES</span></span>

### <span data-ttu-id="b19f8-110">Örnek 1: ağ ile kurtarma ağı arasında eşleme oluşturma</span><span class="sxs-lookup"><span data-stu-id="b19f8-110">Example 1: Create a mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $Networks = Get-AzureSiteRecoveryNetwork -Server $Servers[0]
PS C:\> New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork $Networks[0] -RecoveryNetwork $Networks[1]
```

<span data-ttu-id="b19f8-111">İlk komut cmdlet 'i **Get-AzureSiteRecoveryServer** cmdlet 'ini kullanarak geçerli Azure Site Recovery Kasası için sunucuları alır.</span><span class="sxs-lookup"><span data-stu-id="b19f8-111">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="b19f8-112">Komut, $Servers dizi değişkeninde site kurtarma sunucularını depolar.</span><span class="sxs-lookup"><span data-stu-id="b19f8-112">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="b19f8-113">İkinci komut, **Get-AzureSiteRecoveryNetwork** cmdlet 'ini kullanarak $Servers dizisindeki ilk sunucu için site kurtarma ağını alır.</span><span class="sxs-lookup"><span data-stu-id="b19f8-113">The second command gets the site recovery network for the first server in the $Servers array by using the **Get-AzureSiteRecoveryNetwork** cmdlet.</span></span>
<span data-ttu-id="b19f8-114">Komut, $Networks değişkeninde ağları depolar.</span><span class="sxs-lookup"><span data-stu-id="b19f8-114">The command stores the networks in the $Networks variable.</span></span>

<span data-ttu-id="b19f8-115">Son komutu birincil ağla kurtarma ağı arasında bir eşleme oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b19f8-115">The final command creates a mapping between the primary network and the recovery network.</span></span>
<span data-ttu-id="b19f8-116">Komut birincil ağı $Networks ilk öğesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="b19f8-116">The command specifies the primary network as the first element of $Networks.</span></span>
<span data-ttu-id="b19f8-117">Komut, kurtarma ağını $Networks ikinci öğesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="b19f8-117">The command specifies the recovery network as the second element of $Networks.</span></span>

## <span data-ttu-id="b19f8-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b19f8-118">PARAMETERS</span></span>

### <span data-ttu-id="b19f8-119">-Azuyeniden gönderme Scriptionıd</span><span class="sxs-lookup"><span data-stu-id="b19f8-119">-AzureSubscriptionId</span></span>
<span data-ttu-id="b19f8-120">Azure aboneliğinizin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b19f8-120">Specifies the ID of your Azure subscription.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b19f8-121">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="b19f8-121">-AzureVMNetworkId</span></span>
<span data-ttu-id="b19f8-122">Azure sanal ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b19f8-122">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b19f8-123">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="b19f8-123">-PrimaryNetwork</span></span>
<span data-ttu-id="b19f8-124">Birincil ağ nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b19f8-124">Specifies the primary network object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b19f8-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="b19f8-125">-Profile</span></span>
<span data-ttu-id="b19f8-126">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b19f8-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b19f8-127">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="b19f8-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b19f8-128">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="b19f8-128">-RecoveryNetwork</span></span>
<span data-ttu-id="b19f8-129">Kurtarma ağı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b19f8-129">Specifies the recovery network object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b19f8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b19f8-130">CommonParameters</span></span>
<span data-ttu-id="b19f8-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b19f8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b19f8-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b19f8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b19f8-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b19f8-133">INPUTS</span></span>

## <span data-ttu-id="b19f8-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b19f8-134">OUTPUTS</span></span>

## <span data-ttu-id="b19f8-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b19f8-135">NOTES</span></span>

## <span data-ttu-id="b19f8-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b19f8-136">RELATED LINKS</span></span>

[<span data-ttu-id="b19f8-137">Get-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="b19f8-137">Get-AzureSiteRecoveryNetworkMapping</span></span>](./Get-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="b19f8-138">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="b19f8-138">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)

[<span data-ttu-id="b19f8-139">Remove-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="b19f8-139">Remove-AzureSiteRecoveryNetworkMapping</span></span>](./Remove-AzureSiteRecoveryNetworkMapping.md)


