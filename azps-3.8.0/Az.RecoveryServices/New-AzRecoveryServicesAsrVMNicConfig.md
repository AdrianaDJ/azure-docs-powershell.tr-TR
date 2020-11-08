---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvmnicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
ms.openlocfilehash: f7b6cd7171b6f50ed0f239e733ca98f0ecd5c05a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098164"
---
# <span data-ttu-id="577c1-101">New-AzRecoveryServicesAsrVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="577c1-101">New-AzRecoveryServicesAsrVMNicConfig</span></span>

## <span data-ttu-id="577c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="577c1-102">SYNOPSIS</span></span>
<span data-ttu-id="577c1-103">Yük devretme ve yük devretme ile ilgili yapılandırma ayrıntılarını içeren bir ASR NIC yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="577c1-103">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span>

## <span data-ttu-id="577c1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="577c1-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrVMNicConfig -NicId <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryVMNetworkId <String>] [-RecoveryVMSubnetName <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-EnableAcceleratedNetworkingOnRecovery] [-RecoveryNicStaticIPAddress <String>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoVMNetworkId <String>]
 [-TfoVMSubnetName <String>] [-TfoNetworkSecurityGroupId <String>] [-EnableAcceleratedNetworkingOnTfo]
 [-TfoNicStaticIPAddress <String>] [-TfoPublicIPAddressId <String>] [-TfoLBBackendAddressPoolId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="577c1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="577c1-105">DESCRIPTION</span></span>
<span data-ttu-id="577c1-106">**New-Azrecoveryservicesasrvmsaconfig** cmdlet 'i, yük devretme ve yük devretmenin ilgili ayrıntılarını IÇEREN BIR ASR NIC yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="577c1-106">The **New-AzRecoveryServicesAsrVMNicConfig** cmdlet creates an ASR NIC config object that contains the failover and test failover related details.</span></span> <span data-ttu-id="577c1-107">Herhangi bir bilgi geçirilmemişse, bu değerlerin null olarak güncelleştirilmesine engel olmak için çoğaltma korumalı öğesinden ilgili değerler çekilir.</span><span class="sxs-lookup"><span data-stu-id="577c1-107">In case any information is not passed, the corresponding values are picked from the replication protected item to avoid these values being updated to null.</span></span>

## <span data-ttu-id="577c1-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="577c1-108">EXAMPLES</span></span>

### <span data-ttu-id="577c1-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="577c1-109">Example 1</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -RecoveryNicStaticIPAddress "10.0.0.1" `
    -TfoVMNetworkId $tfoNetworkId -TfoVMSubnetName $tfoSubnetName -TfoNicStaticIPAddress "10.0.1.1"
```

<span data-ttu-id="577c1-110">NIC için yapılandırılmış failover ve test faiover ağ ayarları ile bir ASRVmNicConfig nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="577c1-110">Creates an ASRVmNicConfig object with the failover and test faiover networking settings configured for the NIC.</span></span> <span data-ttu-id="577c1-111">Yukarıda geçen tüm özellikler geçirilen korumalı öğeden alınmıştır.</span><span class="sxs-lookup"><span data-stu-id="577c1-111">Any property that's not passed above is fetched from the protected item passed.</span></span>

## <span data-ttu-id="577c1-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="577c1-112">PARAMETERS</span></span>

### <span data-ttu-id="577c1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="577c1-113">-DefaultProfile</span></span>
<span data-ttu-id="577c1-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="577c1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="577c1-115">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="577c1-115">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="577c1-116">Kurtarma NIC 'de hızlandırılmış ağ özelliğinin etkinleştirilip etkinleştirilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="577c1-116">Specifies whether accelerated networking is enabled on recovery NIC.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="577c1-117">-EnableAcceleratedNetworkingOnTfo</span><span class="sxs-lookup"><span data-stu-id="577c1-117">-EnableAcceleratedNetworkingOnTfo</span></span>
<span data-ttu-id="577c1-118">Test yük devretmesi NIC 'de hızlandırılmış ağ özelliğinin etkinleştirilip etkinleştirilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="577c1-118">Specifies whether accelerated networking is enabled on test failover NIC.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="577c1-119">-NicId</span><span class="sxs-lookup"><span data-stu-id="577c1-119">-NicId</span></span>
<span data-ttu-id="577c1-120">ASR NIC GUID 'INI belirtme.</span><span class="sxs-lookup"><span data-stu-id="577c1-120">Specify the ASR NIC GUID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="577c1-121">-Recoverylbbackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="577c1-121">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="577c1-122">Kurtarma NIC için arka uç adres havuzunun kimliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="577c1-122">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="577c1-123">-Recoverynetworksecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="577c1-123">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="577c1-124">Kurtarma NIC ile ilişkili NSG 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="577c1-124">Specifies the ID of the NSG associated with recovery NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="577c1-125">-Recoverynicstaticıpaddress</span><span class="sxs-lookup"><span data-stu-id="577c1-125">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="577c1-126">Kurtarma NIC 'in IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="577c1-126">Specifies the IP address of the recovery NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="577c1-127">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="577c1-127">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="577c1-128">Kurtarma NIC ile ilişkili ortak IP adresinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="577c1-128">Specifies the ID of the public IP address associated with recovery NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="577c1-129">-Recoveryvmnetworkıd</span><span class="sxs-lookup"><span data-stu-id="577c1-129">-RecoveryVMNetworkId</span></span>
<span data-ttu-id="577c1-130">Kurtarma sanal ağının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="577c1-130">Specifies the ID of the recovery virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="577c1-131">-RecoveryVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="577c1-131">-RecoveryVMSubnetName</span></span>
<span data-ttu-id="577c1-132">Kurtarma alt ağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="577c1-132">Specifies the name of the recovery subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="577c1-133">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="577c1-133">-ReplicationProtectedItem</span></span>
<span data-ttu-id="577c1-134">ASR çoğaltması korumalı öğesini belirtin.</span><span class="sxs-lookup"><span data-stu-id="577c1-134">Specify the ASR Replication Protected Item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="577c1-135">-Tfolbbackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="577c1-135">-TfoLBBackendAddressPoolId</span></span>
<span data-ttu-id="577c1-136">Kurtarma NIC için arka uç adres havuzunun kimliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="577c1-136">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="577c1-137">-Tfsecurityetworksecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="577c1-137">-TfoNetworkSecurityGroupId</span></span>
<span data-ttu-id="577c1-138">Test yük devretmesi ile ilişkili NSG 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="577c1-138">Specifies the ID of the NSG associated with test failover NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="577c1-139">-Tfıcıstaticıpaddress</span><span class="sxs-lookup"><span data-stu-id="577c1-139">-TfoNicStaticIPAddress</span></span>
<span data-ttu-id="577c1-140">Test yük devretmesi NIC 'in IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="577c1-140">Specifies the IP address of the test failover NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="577c1-141">-Tfopublicipadresisid</span><span class="sxs-lookup"><span data-stu-id="577c1-141">-TfoPublicIPAddressId</span></span>
<span data-ttu-id="577c1-142">Test yük devretmesi ile ilişkili ortak IP adresi KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="577c1-142">Specifies the ID of the public IP address associated with test failover NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="577c1-143">-Tfovmnetworkıd</span><span class="sxs-lookup"><span data-stu-id="577c1-143">-TfoVMNetworkId</span></span>
<span data-ttu-id="577c1-144">Test yük devretmesi sanal ağının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="577c1-144">Specifies the ID of the test failover virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="577c1-145">-TfoVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="577c1-145">-TfoVMSubnetName</span></span>
<span data-ttu-id="577c1-146">Test yük devretme alt ağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="577c1-146">Specifies the name of the test failover subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="577c1-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="577c1-147">CommonParameters</span></span>
<span data-ttu-id="577c1-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="577c1-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="577c1-149">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="577c1-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="577c1-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="577c1-150">INPUTS</span></span>

### <span data-ttu-id="577c1-151">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="577c1-151">None</span></span>

## <span data-ttu-id="577c1-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="577c1-152">OUTPUTS</span></span>

### <span data-ttu-id="577c1-153">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="577c1-153">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span></span>

## <span data-ttu-id="577c1-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="577c1-154">NOTES</span></span>

## <span data-ttu-id="577c1-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="577c1-155">RELATED LINKS</span></span>
