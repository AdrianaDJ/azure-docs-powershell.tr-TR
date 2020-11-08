---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: BB36A434-6BE3-46BF-B10A-FCD6C766CB84
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87414a56778123053615bb36a06113e2b0b0633f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106110"
---
# <span data-ttu-id="50ba0-101">Remove-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="50ba0-101">Remove-AzureSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="50ba0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50ba0-102">SYNOPSIS</span></span>
<span data-ttu-id="50ba0-103">Site kurtarma kasasından Ağ eşlemesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="50ba0-103">Removes a network mapping from a Site Recovery vault.</span></span>

## <span data-ttu-id="50ba0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="50ba0-104">SYNTAX</span></span>

```
Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping <ASRNetworkMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="50ba0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="50ba0-105">DESCRIPTION</span></span>
<span data-ttu-id="50ba0-106">**Remove-AzureSiteRecoveryNetworkMapping** cmdlet 'i, geçerli Azure Site Recovery kasasından bir ağ eşlemesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="50ba0-106">The **Remove-AzureSiteRecoveryNetworkMapping** cmdlet removes a network mapping from the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="50ba0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="50ba0-107">EXAMPLES</span></span>

### <span data-ttu-id="50ba0-108">Örnek 1: ağ ile kurtarma ağı arasındaki eşlemeyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="50ba0-108">Example 1: Remove the mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[0]
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

<span data-ttu-id="50ba0-109">İlk komut cmdlet 'i **Get-AzureSiteRecoveryServer** cmdlet 'ini kullanarak geçerli Azure Site Recovery Kasası için sunucuları alır.</span><span class="sxs-lookup"><span data-stu-id="50ba0-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="50ba0-110">Komut, $Servers dizi değişkeninde site kurtarma sunucularını depolar.</span><span class="sxs-lookup"><span data-stu-id="50ba0-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="50ba0-111">İkinci komut birincil ağla kurtarma ağı arasındaki eşlemeyi alır ve $NetworkMapping değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="50ba0-111">The second command gets the mapping between the primary network and the recovery network, and then stores it in the $NetworkMapping variable.</span></span>
<span data-ttu-id="50ba0-112">Komut, $Servers ilk öğesi olarak ağ eşlemesinin birincil sunucusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="50ba0-112">The command specifies the primary server for the network mapping as the first element of $Servers.</span></span>
<span data-ttu-id="50ba0-113">Komut, kurtarma ağının sunucusunu $Servers ikinci öğesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="50ba0-113">The command specifies the server for the recovery network as the second element of $Servers.</span></span>

<span data-ttu-id="50ba0-114">Son komut $NetworkMapping Ağ eşlemesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="50ba0-114">The final command removes the network mapping in $NetworkMapping.</span></span>

### <span data-ttu-id="50ba0-115">Örnek 2: ağ ile Azure sanal makine ağı arasındaki eşlemeyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="50ba0-115">Example 2: Remove the mapping between a network and an Azure virtual machine network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -Azure
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

<span data-ttu-id="50ba0-116">İlk komut cmdlet 'i, geçerli site kurtarma Kasası için sunucuları alır.</span><span class="sxs-lookup"><span data-stu-id="50ba0-116">The first command cmdlet gets servers for the current Site Recovery vault.</span></span>
<span data-ttu-id="50ba0-117">Komut, $Servers dizi değişkeninde site kurtarma sunucularını depolar.</span><span class="sxs-lookup"><span data-stu-id="50ba0-117">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="50ba0-118">İkinci komut birincil ağ ile Azure sanal makine ağı arasındaki eşlemeyi alır ve $NetworkMapping değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="50ba0-118">The second command gets a mapping between the primary network and an Azure virtual machine network, and then stores it in the $NetworkMapping variable.</span></span>
<span data-ttu-id="50ba0-119">Komut, $Servers ilk öğesi olarak ağın birincil sunucusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="50ba0-119">The command specifies the primary server for the network as the first element of $Servers.</span></span>
<span data-ttu-id="50ba0-120">Komut, *Azure* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="50ba0-120">The command specifies the *Azure* parameter.</span></span>
<span data-ttu-id="50ba0-121">Bu nedenle, komut bir Azure sanal makine ağının eşlemesini alır.</span><span class="sxs-lookup"><span data-stu-id="50ba0-121">Therefore, the command gets the mapping to an Azure virtual machine network.</span></span>

<span data-ttu-id="50ba0-122">Son komut $NetworkMapping Ağ eşlemesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="50ba0-122">The final command removes the network mapping in $NetworkMapping.</span></span>

## <span data-ttu-id="50ba0-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="50ba0-123">PARAMETERS</span></span>

### <span data-ttu-id="50ba0-124">-NetworkMapping</span><span class="sxs-lookup"><span data-stu-id="50ba0-124">-NetworkMapping</span></span>
<span data-ttu-id="50ba0-125">Kaldırılacak ağ eşlemesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="50ba0-125">Specifies the network mapping to remove.</span></span>

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50ba0-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="50ba0-126">-Profile</span></span>
<span data-ttu-id="50ba0-127">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="50ba0-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="50ba0-128">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="50ba0-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="50ba0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50ba0-129">CommonParameters</span></span>
<span data-ttu-id="50ba0-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="50ba0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50ba0-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50ba0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50ba0-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="50ba0-132">INPUTS</span></span>

## <span data-ttu-id="50ba0-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="50ba0-133">OUTPUTS</span></span>

## <span data-ttu-id="50ba0-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="50ba0-134">NOTES</span></span>

## <span data-ttu-id="50ba0-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="50ba0-135">RELATED LINKS</span></span>

[<span data-ttu-id="50ba0-136">Get-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="50ba0-136">Get-AzureSiteRecoveryNetworkMapping</span></span>](./Get-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="50ba0-137">New-AzureSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="50ba0-137">New-AzureSiteRecoveryNetworkMapping</span></span>](./New-AzureSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="50ba0-138">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="50ba0-138">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)


