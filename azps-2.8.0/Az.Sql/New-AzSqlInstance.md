---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: d80e6ddd7fa420b07a0df30c2718d9c4e96123fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933838"
---
# <span data-ttu-id="76d2e-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="76d2e-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="76d2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76d2e-102">SYNOPSIS</span></span>
<span data-ttu-id="76d2e-103">Azure SQL veritabanı yönetilen örneği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="76d2e-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="76d2e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76d2e-104">SYNTAX</span></span>

### <span data-ttu-id="76d2e-105">NewByEditionAndComputeGenerationParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="76d2e-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76d2e-106">Newbyınstancepoolparentobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="76d2e-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76d2e-107">Newbyınstancepoolresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="76d2e-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="76d2e-108">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="76d2e-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="76d2e-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="76d2e-109">DESCRIPTION</span></span>
<span data-ttu-id="76d2e-110">**New-Azsqlınstance** cmdlet 'ı BIR Azure SQL veritabanı yönetilen örneği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="76d2e-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="76d2e-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76d2e-111">EXAMPLES</span></span>

### <span data-ttu-id="76d2e-112">Örnek 1: yeni bir örnek oluşturma</span><span class="sxs-lookup"><span data-stu-id="76d2e-112">Example 1: Create a new instance</span></span>
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

<span data-ttu-id="76d2e-113">Bu komut, SkuName parametresini kullanarak yeni bir örnek oluşturur.</span><span class="sxs-lookup"><span data-stu-id="76d2e-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="76d2e-114">Örnek 2: yeni bir örnek oluşturma</span><span class="sxs-lookup"><span data-stu-id="76d2e-114">Example 2: Create a new instance</span></span>
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

<span data-ttu-id="76d2e-115">Bu komut, sürüm ve ComputeGeneration parametrelerini kullanarak yeni bir örnek oluşturur.</span><span class="sxs-lookup"><span data-stu-id="76d2e-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="76d2e-116">Örnek 3: örnek havuz nesnesi kullanarak örnek havuzunda yeni bir örnek oluşturma</span><span class="sxs-lookup"><span data-stu-id="76d2e-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
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

<span data-ttu-id="76d2e-117">Bu komut, örnek havuzu nesnesini kullanan bir örnek havuzunda yeni bir örnek oluşturur.</span><span class="sxs-lookup"><span data-stu-id="76d2e-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="76d2e-118">Örnek 4: örnek havuz kaynak tanımlayıcısını kullanarak örnek havuzda yeni bir örnek oluşturma</span><span class="sxs-lookup"><span data-stu-id="76d2e-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
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

<span data-ttu-id="76d2e-119">Bu komut, örnek havuzunun kaynak tanımlayıcısını kullanarak örnek havuzda yeni bir örnek oluşturur.</span><span class="sxs-lookup"><span data-stu-id="76d2e-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="76d2e-120">Örnek 5: örnek havuzda yeni bir örnek oluşturma</span><span class="sxs-lookup"><span data-stu-id="76d2e-120">Example 5: Create a new instance in an instance pool</span></span>
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

<span data-ttu-id="76d2e-121">Bu komut, instancePool0 adında örnek havuzda yeni bir örnek oluşturur</span><span class="sxs-lookup"><span data-stu-id="76d2e-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

## <span data-ttu-id="76d2e-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76d2e-122">PARAMETERS</span></span>

### <span data-ttu-id="76d2e-123">-\Administrators kimlik bilgisi</span><span class="sxs-lookup"><span data-stu-id="76d2e-123">-AdministratorCredential</span></span>
<span data-ttu-id="76d2e-124">Örneğin SQL kimlik doğrulama kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="76d2e-124">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="76d2e-125">-Iş</span><span class="sxs-lookup"><span data-stu-id="76d2e-125">-AsJob</span></span>
<span data-ttu-id="76d2e-126">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="76d2e-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="76d2e-127">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="76d2e-127">-AssignIdentity</span></span>
<span data-ttu-id="76d2e-128">Azure Keykasa gibi temel yönetim hizmetleriyle kullanılmak üzere bu yönetilen örnek için bir Azure Active Directory kimliği oluşturun ve atayın.</span><span class="sxs-lookup"><span data-stu-id="76d2e-128">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="76d2e-129">-Harmanlama</span><span class="sxs-lookup"><span data-stu-id="76d2e-129">-Collation</span></span>
<span data-ttu-id="76d2e-130">Kullanılacak Azure SQL yönetilen örneğinin harmanlaması.</span><span class="sxs-lookup"><span data-stu-id="76d2e-130">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="76d2e-131">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="76d2e-131">-ComputeGeneration</span></span>
<span data-ttu-id="76d2e-132">Örnek için hesaplama oluşturma.</span><span class="sxs-lookup"><span data-stu-id="76d2e-132">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="76d2e-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76d2e-133">-DefaultProfile</span></span>
<span data-ttu-id="76d2e-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="76d2e-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76d2e-135">-Dnszoneiş ortağı</span><span class="sxs-lookup"><span data-stu-id="76d2e-135">-DnsZonePartner</span></span>
<span data-ttu-id="76d2e-136">Yönetilen örnek oluşturulurken DnsZone özelliğini devralmak için iş ortağı yönetilen sunucusunun kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="76d2e-136">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

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

### <span data-ttu-id="76d2e-137">-Edition</span><span class="sxs-lookup"><span data-stu-id="76d2e-137">-Edition</span></span>
<span data-ttu-id="76d2e-138">Örneğin sürümü.</span><span class="sxs-lookup"><span data-stu-id="76d2e-138">The edition for the instance.</span></span>

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

### <span data-ttu-id="76d2e-139">-Instancepool</span><span class="sxs-lookup"><span data-stu-id="76d2e-139">-InstancePool</span></span>
<span data-ttu-id="76d2e-140">Örnek havuz üst nesnesi.</span><span class="sxs-lookup"><span data-stu-id="76d2e-140">The instance pool parent object.</span></span>

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

### <span data-ttu-id="76d2e-141">-Instancepoolname</span><span class="sxs-lookup"><span data-stu-id="76d2e-141">-InstancePoolName</span></span>
<span data-ttu-id="76d2e-142">Bu örneği yerleştirmek için örnek havuz.</span><span class="sxs-lookup"><span data-stu-id="76d2e-142">The instance pool to place this instance in.</span></span>

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

### <span data-ttu-id="76d2e-143">-Instancepoolresourceıd</span><span class="sxs-lookup"><span data-stu-id="76d2e-143">-InstancePoolResourceId</span></span>
<span data-ttu-id="76d2e-144">Örnek havuz kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="76d2e-144">The instance pool resource id.</span></span>

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

### <span data-ttu-id="76d2e-145">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="76d2e-145">-LicenseType</span></span>
<span data-ttu-id="76d2e-146">Hangi lisans türünün kullanılacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="76d2e-146">Determines which License Type to use.</span></span> <span data-ttu-id="76d2e-147">Olası değerler:</span><span class="sxs-lookup"><span data-stu-id="76d2e-147">Possible values are:</span></span>
- <span data-ttu-id="76d2e-148">Temel fiyat-Azure Karma avantajı (AHB) mevcut SQL Server lisans sahiplerinin indirimli fiyatlandırması uygulanır.</span><span class="sxs-lookup"><span data-stu-id="76d2e-148">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="76d2e-149">Yönetilen örnek hizmeti fiyatı var olan SQL Server lisans sahipleri için düşülecektir.</span><span class="sxs-lookup"><span data-stu-id="76d2e-149">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="76d2e-150">Licenseeklenmiş-Azure Karma avantajı (AHB) mevcut SQL Server lisans sahiplerinin indirim fiyatlandırması uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="76d2e-150">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="76d2e-151">Yönetilen örnek hizmeti fiyatı Yeni bir SQL Server lisans maliyetleri içerir.</span><span class="sxs-lookup"><span data-stu-id="76d2e-151">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="76d2e-152">-Konum</span><span class="sxs-lookup"><span data-stu-id="76d2e-152">-Location</span></span>
<span data-ttu-id="76d2e-153">Örneğin oluşturulacağı konum</span><span class="sxs-lookup"><span data-stu-id="76d2e-153">The location in which to create the instance</span></span>

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

### <span data-ttu-id="76d2e-154">-Ad</span><span class="sxs-lookup"><span data-stu-id="76d2e-154">-Name</span></span>
<span data-ttu-id="76d2e-155">Örnek adı.</span><span class="sxs-lookup"><span data-stu-id="76d2e-155">Instance name.</span></span>

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

### <span data-ttu-id="76d2e-156">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="76d2e-156">-ProxyOverride</span></span>
<span data-ttu-id="76d2e-157">Örneğe bağlanmak için kullanılan bağlantı türü.</span><span class="sxs-lookup"><span data-stu-id="76d2e-157">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="76d2e-158">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="76d2e-158">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="76d2e-159">Örnek için genel veri uç noktasının etkinleştirilip etkinleştirilmediğini.</span><span class="sxs-lookup"><span data-stu-id="76d2e-159">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="76d2e-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76d2e-160">-ResourceGroupName</span></span>
<span data-ttu-id="76d2e-161">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="76d2e-161">The name of the resource group.</span></span>

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

### <span data-ttu-id="76d2e-162">-SkuName</span><span class="sxs-lookup"><span data-stu-id="76d2e-162">-SkuName</span></span>
<span data-ttu-id="76d2e-163">Örneğin ' GP_Gen4 ', ' BC_Gen4 ' örnek adı.</span><span class="sxs-lookup"><span data-stu-id="76d2e-163">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="76d2e-164">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="76d2e-164">-StorageSizeInGB</span></span>
<span data-ttu-id="76d2e-165">Örnekle ilişkilendirilecek depolama boyutu miktarını belirler</span><span class="sxs-lookup"><span data-stu-id="76d2e-165">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="76d2e-166">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="76d2e-166">-SubnetId</span></span>
<span data-ttu-id="76d2e-167">Örnek oluşturma için kullanılacak alt ağ kimliği</span><span class="sxs-lookup"><span data-stu-id="76d2e-167">The Subnet Id to use for instance creation</span></span>

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

### <span data-ttu-id="76d2e-168">Etiketli</span><span class="sxs-lookup"><span data-stu-id="76d2e-168">-Tag</span></span>
<span data-ttu-id="76d2e-169">Örnekle ilişkilendirilecek Etiketler</span><span class="sxs-lookup"><span data-stu-id="76d2e-169">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="76d2e-170">-TimeZoneId</span><span class="sxs-lookup"><span data-stu-id="76d2e-170">-TimezoneId</span></span>
<span data-ttu-id="76d2e-171">Ayarlanacak örnek için saat dilimi kimliği.</span><span class="sxs-lookup"><span data-stu-id="76d2e-171">The time zone id for the instance to set.</span></span> <span data-ttu-id="76d2e-172">Saat dilimi kimliklerinin listesi sys.time_zone_info (Transact-SQL) görünümünde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="76d2e-172">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="76d2e-173">-VCore</span><span class="sxs-lookup"><span data-stu-id="76d2e-173">-VCore</span></span>
<span data-ttu-id="76d2e-174">Örnekle ne kadar Vçekirdeğin ilişkilendiyeceğini belirler</span><span class="sxs-lookup"><span data-stu-id="76d2e-174">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="76d2e-175">-Onay</span><span class="sxs-lookup"><span data-stu-id="76d2e-175">-Confirm</span></span>
<span data-ttu-id="76d2e-176">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="76d2e-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76d2e-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76d2e-177">-WhatIf</span></span>
<span data-ttu-id="76d2e-178">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="76d2e-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76d2e-179">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="76d2e-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76d2e-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76d2e-180">CommonParameters</span></span>
<span data-ttu-id="76d2e-181">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76d2e-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76d2e-182">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="76d2e-182">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76d2e-183">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76d2e-183">INPUTS</span></span>

### <span data-ttu-id="76d2e-184">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="76d2e-184">None</span></span>

## <span data-ttu-id="76d2e-185">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76d2e-185">OUTPUTS</span></span>

### <span data-ttu-id="76d2e-186">Microsoft. Azure. Commands. Sql. ManagedInstance. model. Azureskalite Managedınstancemodel</span><span class="sxs-lookup"><span data-stu-id="76d2e-186">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="76d2e-187">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76d2e-187">NOTES</span></span>

## <span data-ttu-id="76d2e-188">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76d2e-188">RELATED LINKS</span></span>
