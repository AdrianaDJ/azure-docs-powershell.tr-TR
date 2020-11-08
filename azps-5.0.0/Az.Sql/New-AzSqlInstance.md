---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: bb9ae3ba225c67a98b6c3588e1dc0c63f02170ae
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276670"
---
# <span data-ttu-id="3bbe9-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3bbe9-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="3bbe9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bbe9-102">SYNOPSIS</span></span>
<span data-ttu-id="3bbe9-103">Azure SQL veritabanı yönetilen örneği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="3bbe9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3bbe9-104">SYNTAX</span></span>

### <span data-ttu-id="3bbe9-105">NewByEditionAndComputeGenerationParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3bbe9-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-MinimalTlsVersion <String>]
 [-BackupStorageRedundancy <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bbe9-106">Newbyınstancepoolparentobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="3bbe9-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bbe9-107">Newbyınstancepoolresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="3bbe9-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bbe9-108">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="3bbe9-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bbe9-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="3bbe9-109">DESCRIPTION</span></span>
<span data-ttu-id="3bbe9-110">**New-Azsqlınstance** cmdlet 'ı BIR Azure SQL veritabanı yönetilen örneği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="3bbe9-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3bbe9-111">EXAMPLES</span></span>

### <span data-ttu-id="3bbe9-112">Örnek 1: yeni bir örnek oluşturma</span><span class="sxs-lookup"><span data-stu-id="3bbe9-112">Example 1: Create a new instance</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -SkuName GP_Gen4 -DnsZonePartner "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/partnerServerForDnsZone"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 16
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         :
```

<span data-ttu-id="3bbe9-113">Bu komut, SkuName parametresini kullanarak yeni bir örnek oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="3bbe9-114">Örnek 2: yeni bir örnek oluşturma</span><span class="sxs-lookup"><span data-stu-id="3bbe9-114">Example 2: Create a new instance</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance2 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -Edition "GeneralPurpose" -ComputeGeneration Gen4
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 16
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         :
```

<span data-ttu-id="3bbe9-115">Bu komut, sürüm ve ComputeGeneration parametrelerini kullanarak yeni bir örnek oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="3bbe9-116">Örnek 3: örnek havuz nesnesi kullanarak örnek havuzunda yeni bir örnek oluşturma</span><span class="sxs-lookup"><span data-stu-id="3bbe9-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancepool0
PS C:\> $instancePool | New-AzSqlInstance -Name managedInstance2 -AdministratorCredential (Get-Credential) -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 2
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 2
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         : instancepool0
```

<span data-ttu-id="3bbe9-117">Bu komut, örnek havuzu nesnesini kullanan bir örnek havuzunda yeni bir örnek oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="3bbe9-118">Örnek 4: örnek havuz kaynak tanımlayıcısını kullanarak örnek havuzda yeni bir örnek oluşturma</span><span class="sxs-lookup"><span data-stu-id="3bbe9-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
```powershell
PS C:\> $instancePool | New-AzSqlInstance -Name managedInstance2 -AdministratorCredential (Get-Credential) -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 2 -InstancePoolResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 2
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         : instancepool0
```

<span data-ttu-id="3bbe9-119">Bu komut, örnek havuzunun kaynak tanımlayıcısını kullanarak örnek havuzda yeni bir örnek oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="3bbe9-120">Örnek 5: örnek havuzda yeni bir örnek oluşturma</span><span class="sxs-lookup"><span data-stu-id="3bbe9-120">Example 5: Create a new instance in an instance pool</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName resourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 32 -VCore 2 -ComputeGeneration Gen5 -Edition GeneralPurpose -InstancePoolName instancePool0
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 2
StorageSizeInGB          : 32
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0
```

<span data-ttu-id="3bbe9-121">Bu komut, instancePool0 adında örnek havuzda yeni bir örnek oluşturur</span><span class="sxs-lookup"><span data-stu-id="3bbe9-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

## <span data-ttu-id="3bbe9-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3bbe9-122">PARAMETERS</span></span>

### <span data-ttu-id="3bbe9-123">-\Administrators kimlik bilgisi</span><span class="sxs-lookup"><span data-stu-id="3bbe9-123">-AdministratorCredential</span></span>
<span data-ttu-id="3bbe9-124">Örneğin SQL kimlik doğrulama kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-124">The SQL authentication credential of the instance.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bbe9-125">-Iş</span><span class="sxs-lookup"><span data-stu-id="3bbe9-125">-AsJob</span></span>
<span data-ttu-id="3bbe9-126">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="3bbe9-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3bbe9-127">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="3bbe9-127">-AssignIdentity</span></span>
<span data-ttu-id="3bbe9-128">Azure Keykasa gibi temel yönetim hizmetleriyle kullanılmak üzere bu yönetilen örnek için bir Azure Active Directory kimliği oluşturun ve atayın.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-128">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="3bbe9-129">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="3bbe9-129">-BackupStorageRedundancy</span></span>
<span data-ttu-id="3bbe9-130">SQL Azure yönetilen örneğinin yedeklerini depolamak için kullanılan yedek depolama yedeği.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-130">The Backup storage redundancy used to store backups for the Sql Azure Managed Instance.</span></span> <span data-ttu-id="3bbe9-131">Seçenekler şunlardır: yerel, bölge ve coğrafi</span><span class="sxs-lookup"><span data-stu-id="3bbe9-131">Options are: Local, Zone and Geo</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bbe9-132">-Harmanlama</span><span class="sxs-lookup"><span data-stu-id="3bbe9-132">-Collation</span></span>
<span data-ttu-id="3bbe9-133">Kullanılacak Azure SQL yönetilen örneğinin harmanlaması.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-133">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="3bbe9-134">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="3bbe9-134">-ComputeGeneration</span></span>
<span data-ttu-id="3bbe9-135">Örnek için hesaplama oluşturma.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-135">The compute generation for the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bbe9-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bbe9-136">-DefaultProfile</span></span>
<span data-ttu-id="3bbe9-137">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bbe9-138">-Dnszoneiş ortağı</span><span class="sxs-lookup"><span data-stu-id="3bbe9-138">-DnsZonePartner</span></span>
<span data-ttu-id="3bbe9-139">Yönetilen örnek oluşturulurken DnsZone özelliğini devralmak için iş ortağı yönetilen sunucusunun kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="3bbe9-139">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

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

### <span data-ttu-id="3bbe9-140">-Edition</span><span class="sxs-lookup"><span data-stu-id="3bbe9-140">-Edition</span></span>
<span data-ttu-id="3bbe9-141">Örneğin sürümü.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-141">The edition for the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bbe9-142">-Force</span><span class="sxs-lookup"><span data-stu-id="3bbe9-142">-Force</span></span>
<span data-ttu-id="3bbe9-143">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="3bbe9-143">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="3bbe9-144">-Instancepool</span><span class="sxs-lookup"><span data-stu-id="3bbe9-144">-InstancePool</span></span>
<span data-ttu-id="3bbe9-145">Örnek havuz üst nesnesi.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-145">The instance pool parent object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: NewByInstancePoolParentObjectParameterSet
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3bbe9-146">-Instancepoolname</span><span class="sxs-lookup"><span data-stu-id="3bbe9-146">-InstancePoolName</span></span>
<span data-ttu-id="3bbe9-147">Bu örneği yerleştirmek için örnek havuz.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-147">The instance pool to place this instance in.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bbe9-148">-Instancepoolresourceıd</span><span class="sxs-lookup"><span data-stu-id="3bbe9-148">-InstancePoolResourceId</span></span>
<span data-ttu-id="3bbe9-149">Örnek havuz kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-149">The instance pool resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByInstancePoolResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bbe9-150">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="3bbe9-150">-LicenseType</span></span>
<span data-ttu-id="3bbe9-151">Hangi lisans türünün kullanılacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-151">Determines which License Type to use.</span></span> <span data-ttu-id="3bbe9-152">Olası değerler:</span><span class="sxs-lookup"><span data-stu-id="3bbe9-152">Possible values are:</span></span>
- <span data-ttu-id="3bbe9-153">Temel fiyat-Azure Karma avantajı (AHB) mevcut SQL Server lisans sahiplerinin indirimli fiyatlandırması uygulanır.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-153">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="3bbe9-154">Yönetilen örnek hizmeti fiyatı var olan SQL Server lisans sahipleri için düşülecektir.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-154">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="3bbe9-155">Licenseeklenmiş-Azure Karma avantajı (AHB) mevcut SQL Server lisans sahiplerinin indirim fiyatlandırması uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-155">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="3bbe9-156">Yönetilen örnek hizmeti fiyatı Yeni bir SQL Server lisans maliyetleri içerir.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-156">Managed Instance service price will include a new SQL Server license costs.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bbe9-157">-Konum</span><span class="sxs-lookup"><span data-stu-id="3bbe9-157">-Location</span></span>
<span data-ttu-id="3bbe9-158">Örneğin oluşturulacağı konum</span><span class="sxs-lookup"><span data-stu-id="3bbe9-158">The location in which to create the instance</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bbe9-159">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="3bbe9-159">-MinimalTlsVersion</span></span>
<span data-ttu-id="3bbe9-160">Yönetilen örneğe uygulanacak en az TLS sürümü</span><span class="sxs-lookup"><span data-stu-id="3bbe9-160">The minimal TLS version to enforce for Managed instance</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, 1.0, 1.1, 1.2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bbe9-161">-Ad</span><span class="sxs-lookup"><span data-stu-id="3bbe9-161">-Name</span></span>
<span data-ttu-id="3bbe9-162">Örnek adı.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-162">Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bbe9-163">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="3bbe9-163">-ProxyOverride</span></span>
<span data-ttu-id="3bbe9-164">Örneğe bağlanmak için kullanılan bağlantı türü.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-164">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="3bbe9-165">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="3bbe9-165">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="3bbe9-166">Örnek için genel veri uç noktasının etkinleştirilip etkinleştirilmediğini.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-166">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="3bbe9-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bbe9-167">-ResourceGroupName</span></span>
<span data-ttu-id="3bbe9-168">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-168">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bbe9-169">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3bbe9-169">-SkuName</span></span>
<span data-ttu-id="3bbe9-170">Örneğin ' GP_Gen4 ', ' BC_Gen4 ' örnek adı.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-170">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

```yaml
Type: System.String
Parameter Sets: NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bbe9-171">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="3bbe9-171">-StorageSizeInGB</span></span>
<span data-ttu-id="3bbe9-172">Örnekle ilişkilendirilecek depolama boyutu miktarını belirler</span><span class="sxs-lookup"><span data-stu-id="3bbe9-172">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bbe9-173">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="3bbe9-173">-SubnetId</span></span>
<span data-ttu-id="3bbe9-174">Örnek oluşturma için kullanılacak alt ağ kimliği</span><span class="sxs-lookup"><span data-stu-id="3bbe9-174">The Subnet Id to use for instance creation</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bbe9-175">Etiketli</span><span class="sxs-lookup"><span data-stu-id="3bbe9-175">-Tag</span></span>
<span data-ttu-id="3bbe9-176">Örnekle ilişkilendirilecek Etiketler</span><span class="sxs-lookup"><span data-stu-id="3bbe9-176">The tags to associate with the instance</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bbe9-177">-TimeZoneId</span><span class="sxs-lookup"><span data-stu-id="3bbe9-177">-TimezoneId</span></span>
<span data-ttu-id="3bbe9-178">Ayarlanacak örnek için saat dilimi kimliği.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-178">The time zone id for the instance to set.</span></span> <span data-ttu-id="3bbe9-179">Saat dilimi kimliklerinin listesi sys.time_zone_info (Transact-SQL) görünümünde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-179">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="3bbe9-180">-VCore</span><span class="sxs-lookup"><span data-stu-id="3bbe9-180">-VCore</span></span>
<span data-ttu-id="3bbe9-181">Örnekle ne kadar Vçekirdeğin ilişkilendiyeceğini belirler</span><span class="sxs-lookup"><span data-stu-id="3bbe9-181">Determines how much VCore to associate with instance</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bbe9-182">-Onay</span><span class="sxs-lookup"><span data-stu-id="3bbe9-182">-Confirm</span></span>
<span data-ttu-id="3bbe9-183">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bbe9-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bbe9-184">-WhatIf</span></span>
<span data-ttu-id="3bbe9-185">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bbe9-186">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bbe9-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bbe9-187">CommonParameters</span></span>
<span data-ttu-id="3bbe9-188">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bbe9-189">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3bbe9-189">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bbe9-190">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3bbe9-190">INPUTS</span></span>

### <span data-ttu-id="3bbe9-191">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3bbe9-191">None</span></span>

## <span data-ttu-id="3bbe9-192">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3bbe9-192">OUTPUTS</span></span>

### <span data-ttu-id="3bbe9-193">Microsoft. Azure. Commands. Sql. ManagedInstance. model. Azureskalite Managedınstancemodel</span><span class="sxs-lookup"><span data-stu-id="3bbe9-193">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="3bbe9-194">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3bbe9-194">NOTES</span></span>

## <span data-ttu-id="3bbe9-195">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3bbe9-195">RELATED LINKS</span></span>
