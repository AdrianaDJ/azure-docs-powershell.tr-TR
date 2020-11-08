---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: F6C01C25-655C-4798-9826-F7CB168181C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: bc8b7dc7e23a98111e75c2b2c9c079f010e3c5dc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105590"
---
# <span data-ttu-id="fcbf3-101">Get-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="fcbf3-101">Get-AzureSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="fcbf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcbf3-102">SYNOPSIS</span></span>
<span data-ttu-id="fcbf3-103">Site kurtarma Kasası için ağ eşlemelerini alır.</span><span class="sxs-lookup"><span data-stu-id="fcbf3-103">Gets network mappings for a Site Recovery vault.</span></span>

## <span data-ttu-id="fcbf3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fcbf3-104">SYNTAX</span></span>

### <span data-ttu-id="fcbf3-105">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="fcbf3-105">EnterpriseToEnterprise</span></span>
```
Get-AzureSiteRecoveryNetworkMapping -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="fcbf3-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="fcbf3-106">EnterpriseToAzure</span></span>
```
Get-AzureSiteRecoveryNetworkMapping -PrimaryServer <ASRServer> [-Azure] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="fcbf3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fcbf3-107">DESCRIPTION</span></span>
<span data-ttu-id="fcbf3-108">**Get-AzureSiteRecoveryNetworkMapping** cmdlet 'i, geçerli site kurtarma Kasası Için Azure Site Recovery ağ eşlemeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="fcbf3-108">The **Get-AzureSiteRecoveryNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the current Site Recovery vault.</span></span>

## <span data-ttu-id="fcbf3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fcbf3-109">EXAMPLES</span></span>

### <span data-ttu-id="fcbf3-110">Örnek 1: ağ ile kurtarma ağı arasındaki eşlemeyi alma</span><span class="sxs-lookup"><span data-stu-id="fcbf3-110">Example 1: Get the mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[0]
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryNetworkId    : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
PrimaryNetworkName  : phase2RecoveryVMNetwork
RecoveryServerId    : 774859b0-1966-48cc-9df7-759c441b7a8c
RecoveryNetworkId   : d903e2c6-3141-4cef-bfe1-04616cd43cbb
RecoveryNetworkName : phase2PrimaryVMNetwork
PairingStatus       : OK
```

<span data-ttu-id="fcbf3-111">İlk komut cmdlet 'i **Get-AzureSiteRecoveryServer** cmdlet 'ini kullanarak geçerli Azure Site Recovery Kasası için sunucuları alır.</span><span class="sxs-lookup"><span data-stu-id="fcbf3-111">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="fcbf3-112">Komut, $Servers dizi değişkeninde site kurtarma sunucularını depolar.</span><span class="sxs-lookup"><span data-stu-id="fcbf3-112">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="fcbf3-113">İkinci komut birincil ağla kurtarma ağı arasındaki eşlemeyi alır.</span><span class="sxs-lookup"><span data-stu-id="fcbf3-113">The second command gets the mapping between the primary network and the recovery network.</span></span>
<span data-ttu-id="fcbf3-114">Komut, $Servers ilk öğesi olarak ağ eşlemesinin birincil sunucusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="fcbf3-114">The command specifies the primary server for the network mapping as the first element of $Servers.</span></span>
<span data-ttu-id="fcbf3-115">Komut, kurtarma ağının sunucusunu $Servers ikinci öğesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="fcbf3-115">The command specifies the server for the recovery network as the second element of $Servers.</span></span>

### <span data-ttu-id="fcbf3-116">Örnek 2: bir ağ ile Azure sanal makine ağı arasındaki eşlemeyi alma</span><span class="sxs-lookup"><span data-stu-id="fcbf3-116">Example 2: Get the mapping between a network and an Azure virtual machine network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetworkMapping -Azure -PrimaryServer $Servers[0] 
PrimaryServerId     : 774859b0-1966-48cc-9df7-759c441b7a8c
PrimaryNetworkId    : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
PrimaryNetworkName  : phase2RecoveryVMNetwork
RecoveryServerId    : 21a9403c-6ec1-44f2-b744-b4e50b792387
RecoveryNetworkId   : ecb3a462-664f-4f57-873e-d09b5925e1a1
RecoveryNetworkName : AzureVMNetwork
PairingStatus       : OK
```

<span data-ttu-id="fcbf3-117">İlk komut cmdlet 'i, geçerli site kurtarma Kasası için sunucuları alır.</span><span class="sxs-lookup"><span data-stu-id="fcbf3-117">The first command cmdlet gets servers for the current Site Recovery vault.</span></span>
<span data-ttu-id="fcbf3-118">Komut, $Servers dizi değişkeninde sunucuları depolar.</span><span class="sxs-lookup"><span data-stu-id="fcbf3-118">The command stores the servers in the $Servers array variable.</span></span>

<span data-ttu-id="fcbf3-119">İkinci komut birincil ağ ile Azure sanal makine ağı arasındaki eşlemeyi alır.</span><span class="sxs-lookup"><span data-stu-id="fcbf3-119">The second command gets a mapping between the primary network and an Azure virtual machine network.</span></span>
<span data-ttu-id="fcbf3-120">Komut, $Servers ilk öğesi olarak ağın birincil sunucusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="fcbf3-120">The command specifies the primary server for the network as the first element of $Servers.</span></span>
<span data-ttu-id="fcbf3-121">Komut, *Azure* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fcbf3-121">The command specifies the *Azure* parameter.</span></span>
<span data-ttu-id="fcbf3-122">Bu nedenle, komut bir Azure sanal makine ağının eşlemesini alır.</span><span class="sxs-lookup"><span data-stu-id="fcbf3-122">Therefore, the command gets the mapping to an Azure virtual machine network.</span></span>

## <span data-ttu-id="fcbf3-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fcbf3-123">PARAMETERS</span></span>

### <span data-ttu-id="fcbf3-124">-Azure</span><span class="sxs-lookup"><span data-stu-id="fcbf3-124">-Azure</span></span>
<span data-ttu-id="fcbf3-125">Bu cmdlet 'in Azure sanal ağlarına eşlenmiş birincil sunucudaki ağlar için ağ eşlemelerini aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fcbf3-125">Indicates that this cmdlet gets network mappings for networks on the primary server mapped to Azure virtual networks.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcbf3-126">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="fcbf3-126">-PrimaryServer</span></span>
<span data-ttu-id="fcbf3-127">Eşleşmelerin alınacağı birincil sunucuyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="fcbf3-127">Specifies a primary server for which to get mappings.</span></span>

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

### <span data-ttu-id="fcbf3-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="fcbf3-128">-Profile</span></span>
<span data-ttu-id="fcbf3-129">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fcbf3-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fcbf3-130">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="fcbf3-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fcbf3-131">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="fcbf3-131">-RecoveryServer</span></span>
<span data-ttu-id="fcbf3-132">Eşleşmelerin alınacağı bir kurtarma sunucusu belirtir.</span><span class="sxs-lookup"><span data-stu-id="fcbf3-132">Specifies a recovery server for which to get mappings.</span></span>

```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcbf3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcbf3-133">CommonParameters</span></span>
<span data-ttu-id="fcbf3-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fcbf3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcbf3-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcbf3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcbf3-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fcbf3-136">INPUTS</span></span>

## <span data-ttu-id="fcbf3-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fcbf3-137">OUTPUTS</span></span>

## <span data-ttu-id="fcbf3-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fcbf3-138">NOTES</span></span>

## <span data-ttu-id="fcbf3-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fcbf3-139">RELATED LINKS</span></span>

[<span data-ttu-id="fcbf3-140">New-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="fcbf3-140">New-AzureSiteRecoveryNetworkMapping</span></span>](./New-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="fcbf3-141">Remove-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="fcbf3-141">Remove-AzureSiteRecoveryNetworkMapping</span></span>](./Remove-AzureSiteRecoveryNetworkMapping.md)


