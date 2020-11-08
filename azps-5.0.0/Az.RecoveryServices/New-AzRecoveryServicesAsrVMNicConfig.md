---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvmnicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
ms.openlocfilehash: 658a0cfa66abd71a63edc67ab2615713ac815bcd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277042"
---
# <span data-ttu-id="1188a-101">New-AzRecoveryServicesAsrVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="1188a-101">New-AzRecoveryServicesAsrVMNicConfig</span></span>

## <span data-ttu-id="1188a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1188a-102">SYNOPSIS</span></span>
<span data-ttu-id="1188a-103">Yük devretme ve yük devretme ile ilgili yapılandırma ayrıntılarını içeren bir ASR NIC yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1188a-103">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span>

## <span data-ttu-id="1188a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1188a-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrVMNicConfig -NicId <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryVMNetworkId <String>] [-RecoveryNicName <String>] [-RecoveryNicResourceGroupName <String>]
 [-ReuseExistingNic] [-RecoveryVMSubnetName <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-EnableAcceleratedNetworkingOnRecovery] [-RecoveryNicStaticIPAddress <String>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoVMNetworkId <String>]
 [-TfoNicName <String>] [-TfoNicResourceGroupName <String>] [-TfoReuseExistingNic] [-TfoVMSubnetName <String>]
 [-TfoNetworkSecurityGroupId <String>] [-EnableAcceleratedNetworkingOnTfo] [-TfoNicStaticIPAddress <String>]
 [-TfoPublicIPAddressId <String>] [-TfoLBBackendAddressPoolId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1188a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1188a-105">DESCRIPTION</span></span>
<span data-ttu-id="1188a-106">**New-Azrecoveryservicesasrvmsaconfig** cmdlet 'i, yük devretme ve yük devretmenin ilgili ayrıntılarını IÇEREN BIR ASR NIC yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1188a-106">The **New-AzRecoveryServicesAsrVMNicConfig** cmdlet creates an ASR NIC config object that contains the failover and test failover related details.</span></span> <span data-ttu-id="1188a-107">Herhangi bir bilgi geçirilmemişse, bu değerlerin null olarak güncelleştirilmesine engel olmak için çoğaltma korumalı öğesinden ilgili değerler çekilir.</span><span class="sxs-lookup"><span data-stu-id="1188a-107">In case any information is not passed, the corresponding values are picked from the replication protected item to avoid these values being updated to null.</span></span>

## <span data-ttu-id="1188a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1188a-108">EXAMPLES</span></span>

### <span data-ttu-id="1188a-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1188a-109">Example 1</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -RecoveryNicStaticIPAddress "10.0.0.1" `
    -TfoVMNetworkId $tfoNetworkId -TfoVMSubnetName $tfoSubnetName -TfoNicStaticIPAddress "10.0.1.1"
```

<span data-ttu-id="1188a-110">NIC için yapılandırılmış failover ve test faiover ağ ayarları ile bir ASRVmNicConfig nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1188a-110">Creates an ASRVmNicConfig object with the failover and test faiover networking settings configured for the NIC.</span></span> <span data-ttu-id="1188a-111">Yukarıda geçen tüm özellikler geçirilen korumalı öğeden alınmıştır.</span><span class="sxs-lookup"><span data-stu-id="1188a-111">Any property that's not passed above is fetched from the protected item passed.</span></span>

### <span data-ttu-id="1188a-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1188a-112">Example 2</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -TfoNicName $TfoNicName -TfoNicResourceGroupName $TfoNicRgName -TfoReuseExistingNic
```

<span data-ttu-id="1188a-113">NIC yeniden adlandırma için yapılandırılmış test faiover ağ ayarları ile bir ASRVmNicConfig nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1188a-113">Creates an ASRVmNicConfig object with the test faiover networking settings configured for the NIC renaming.</span></span> <span data-ttu-id="1188a-114">Yukarıda geçen tüm özellikler geçirilen korumalı öğeden alınmıştır.</span><span class="sxs-lookup"><span data-stu-id="1188a-114">Any property that's not passed above is fetched from the protected item passed.</span></span>


### <span data-ttu-id="1188a-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="1188a-115">Example 3</span></span>

<span data-ttu-id="1188a-116">Yük devretme ve yük devretme ile ilgili yapılandırma ayrıntılarını içeren bir ASR NIC yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1188a-116">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span> <span data-ttu-id="1188a-117">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="1188a-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -RecoveryNetworkSecurityGroupId <String> -RecoveryNicStaticIPAddress '10.0.0.1' -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -ReplicationProtectedItem $Rpi -TfoNetworkSecurityGroupId <String> -TfoNicStaticIPAddress <String> -TfoVMNetworkId <String> -TfoVMSubnetName <String>
```

## <span data-ttu-id="1188a-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1188a-118">PARAMETERS</span></span>

### <span data-ttu-id="1188a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1188a-119">-DefaultProfile</span></span>
<span data-ttu-id="1188a-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1188a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1188a-121">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="1188a-121">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="1188a-122">Kurtarma NIC 'de hızlandırılmış ağ özelliğinin etkinleştirilip etkinleştirilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1188a-122">Specifies whether accelerated networking is enabled on recovery NIC.</span></span>

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

### <span data-ttu-id="1188a-123">-EnableAcceleratedNetworkingOnTfo</span><span class="sxs-lookup"><span data-stu-id="1188a-123">-EnableAcceleratedNetworkingOnTfo</span></span>
<span data-ttu-id="1188a-124">Test yük devretmesi NIC 'de hızlandırılmış ağ özelliğinin etkinleştirilip etkinleştirilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1188a-124">Specifies whether accelerated networking is enabled on test failover NIC.</span></span>

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

### <span data-ttu-id="1188a-125">-NicId</span><span class="sxs-lookup"><span data-stu-id="1188a-125">-NicId</span></span>
<span data-ttu-id="1188a-126">ASR NIC GUID 'INI belirtme.</span><span class="sxs-lookup"><span data-stu-id="1188a-126">Specify the ASR NIC GUID.</span></span>

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

### <span data-ttu-id="1188a-127">-Recoverylbbackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="1188a-127">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="1188a-128">Kurtarma NIC için arka uç adres havuzunun kimliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1188a-128">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="1188a-129">-Recoverynetworksecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="1188a-129">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="1188a-130">Kurtarma NIC ile ilişkili NSG 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1188a-130">Specifies the ID of the NSG associated with recovery NIC.</span></span>

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

### <span data-ttu-id="1188a-131">-RecoveryNicName</span><span class="sxs-lookup"><span data-stu-id="1188a-131">-RecoveryNicName</span></span>
<span data-ttu-id="1188a-132">Kurtarma NIC 'in adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1188a-132">Specifies the name of the recovery NIC.</span></span>

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

### <span data-ttu-id="1188a-133">-RecoveryNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1188a-133">-RecoveryNicResourceGroupName</span></span>
<span data-ttu-id="1188a-134">Kurtarma NIC kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1188a-134">Specifies the name of the recovery NIC resource group.</span></span>

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

### <span data-ttu-id="1188a-135">-Recoverynicstaticıpaddress</span><span class="sxs-lookup"><span data-stu-id="1188a-135">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="1188a-136">Kurtarma NIC 'in IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1188a-136">Specifies the IP address of the recovery NIC.</span></span>

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

### <span data-ttu-id="1188a-137">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="1188a-137">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="1188a-138">Kurtarma NIC ile ilişkili ortak IP adresinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1188a-138">Specifies the ID of the public IP address associated with recovery NIC.</span></span>

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

### <span data-ttu-id="1188a-139">-Recoveryvmnetworkıd</span><span class="sxs-lookup"><span data-stu-id="1188a-139">-RecoveryVMNetworkId</span></span>
<span data-ttu-id="1188a-140">Kurtarma sanal ağının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1188a-140">Specifies the ID of the recovery virtual network.</span></span>

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

### <span data-ttu-id="1188a-141">-RecoveryVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="1188a-141">-RecoveryVMSubnetName</span></span>
<span data-ttu-id="1188a-142">Kurtarma alt ağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1188a-142">Specifies the name of the recovery subnet.</span></span>

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

### <span data-ttu-id="1188a-143">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="1188a-143">-ReplicationProtectedItem</span></span>
<span data-ttu-id="1188a-144">ASR çoğaltması korumalı öğesini belirtin.</span><span class="sxs-lookup"><span data-stu-id="1188a-144">Specify the ASR Replication Protected Item.</span></span>

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

### <span data-ttu-id="1188a-145">-Reuseexistingnıc</span><span class="sxs-lookup"><span data-stu-id="1188a-145">-ReuseExistingNic</span></span>
<span data-ttu-id="1188a-146">Mevcut bir NIC 'in yük devretme sırasında kullanılıp kullanılamayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1188a-146">Specifies whether an existing NIC can be used during failover.</span></span>

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

### <span data-ttu-id="1188a-147">-Tfolbbackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="1188a-147">-TfoLBBackendAddressPoolId</span></span>
<span data-ttu-id="1188a-148">Kurtarma NIC için arka uç adres havuzunun kimliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1188a-148">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="1188a-149">-Tfsecurityetworksecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="1188a-149">-TfoNetworkSecurityGroupId</span></span>
<span data-ttu-id="1188a-150">Test yük devretmesi ile ilişkili NSG 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1188a-150">Specifies the ID of the NSG associated with test failover NIC.</span></span>

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

### <span data-ttu-id="1188a-151">-Tfııname</span><span class="sxs-lookup"><span data-stu-id="1188a-151">-TfoNicName</span></span>
<span data-ttu-id="1188a-152">Test yük devretmesi NIC 'in adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1188a-152">Specifies the name of the test failover NIC.</span></span>

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

### <span data-ttu-id="1188a-153">-Tfıresourcekaynakgrupadı</span><span class="sxs-lookup"><span data-stu-id="1188a-153">-TfoNicResourceGroupName</span></span>
<span data-ttu-id="1188a-154">Test yük devretmesi NIC kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1188a-154">Specifies the name of the test failover NIC resource group.</span></span>

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

### <span data-ttu-id="1188a-155">-Tfıcıstaticıpaddress</span><span class="sxs-lookup"><span data-stu-id="1188a-155">-TfoNicStaticIPAddress</span></span>
<span data-ttu-id="1188a-156">Test yük devretmesi NIC 'in IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1188a-156">Specifies the IP address of the test failover NIC.</span></span>

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

### <span data-ttu-id="1188a-157">-Tfopublicipadresisid</span><span class="sxs-lookup"><span data-stu-id="1188a-157">-TfoPublicIPAddressId</span></span>
<span data-ttu-id="1188a-158">Test yük devretmesi ile ilişkili ortak IP adresi KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1188a-158">Specifies the ID of the public IP address associated with test failover NIC.</span></span>

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

### <span data-ttu-id="1188a-159">-Tforeexistingnıc</span><span class="sxs-lookup"><span data-stu-id="1188a-159">-TfoReuseExistingNic</span></span>
<span data-ttu-id="1188a-160">Test yük devretmesi sırasında mevcut bir NIC kullanılıp kullanılamayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1188a-160">Specifies whether an existing NIC can be used during test failover.</span></span>

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

### <span data-ttu-id="1188a-161">-Tfovmnetworkıd</span><span class="sxs-lookup"><span data-stu-id="1188a-161">-TfoVMNetworkId</span></span>
<span data-ttu-id="1188a-162">Test yük devretmesi sanal ağının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1188a-162">Specifies the ID of the test failover virtual network.</span></span>

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

### <span data-ttu-id="1188a-163">-TfoVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="1188a-163">-TfoVMSubnetName</span></span>
<span data-ttu-id="1188a-164">Test yük devretme alt ağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1188a-164">Specifies the name of the test failover subnet.</span></span>

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

### <span data-ttu-id="1188a-165">-Onay</span><span class="sxs-lookup"><span data-stu-id="1188a-165">-Confirm</span></span>
<span data-ttu-id="1188a-166">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1188a-166">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1188a-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1188a-167">-WhatIf</span></span>
<span data-ttu-id="1188a-168">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1188a-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1188a-169">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1188a-169">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1188a-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1188a-170">CommonParameters</span></span>
<span data-ttu-id="1188a-171">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1188a-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1188a-172">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1188a-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1188a-173">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1188a-173">INPUTS</span></span>

### <span data-ttu-id="1188a-174">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1188a-174">None</span></span>

## <span data-ttu-id="1188a-175">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1188a-175">OUTPUTS</span></span>

### <span data-ttu-id="1188a-176">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="1188a-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span></span>

## <span data-ttu-id="1188a-177">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1188a-177">NOTES</span></span>

## <span data-ttu-id="1188a-178">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1188a-178">RELATED LINKS</span></span>
