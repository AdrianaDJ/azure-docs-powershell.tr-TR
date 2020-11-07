---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: bfa1785004e13400395bd6a6fc93bdec29a69809
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758891"
---
# <span data-ttu-id="876c3-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="876c3-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="876c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="876c3-102">SYNOPSIS</span></span>
<span data-ttu-id="876c3-103">Azure SQL veritabanı yönetilen örneği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="876c3-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="876c3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="876c3-104">SYNTAX</span></span>

### <span data-ttu-id="876c3-105">NewByEditionAndComputeGenerationParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="876c3-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="876c3-106">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="876c3-106">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="876c3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="876c3-107">DESCRIPTION</span></span>
<span data-ttu-id="876c3-108">**New-Azsqlınstance** cmdlet 'ı BIR Azure SQL veritabanı yönetilen örneği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="876c3-108">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="876c3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="876c3-109">EXAMPLES</span></span>

### <span data-ttu-id="876c3-110">Örnek 1: yeni bir örnek oluşturma</span><span class="sxs-lookup"><span data-stu-id="876c3-110">Example 1: Create a new instance</span></span>
```
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -SkuName GP_Gen4
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
```

<span data-ttu-id="876c3-111">Bu komut, sürüm ve ComputeGeneration parametrelerini kullanarak yeni bir örnek oluşturur.</span><span class="sxs-lookup"><span data-stu-id="876c3-111">This command creates a new instance by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="876c3-112">Örnek 2: yeni bir örnek oluşturma</span><span class="sxs-lookup"><span data-stu-id="876c3-112">Example 2: Create a new instance</span></span>
```
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
```

<span data-ttu-id="876c3-113">Bu komut, sürüm ve ComputeGeneration parametrelerini kullanarak yeni bir örnek oluşturur.</span><span class="sxs-lookup"><span data-stu-id="876c3-113">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

## <span data-ttu-id="876c3-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="876c3-114">PARAMETERS</span></span>

### <span data-ttu-id="876c3-115">-\Administrators kimlik bilgisi</span><span class="sxs-lookup"><span data-stu-id="876c3-115">-AdministratorCredential</span></span>
<span data-ttu-id="876c3-116">Örneğin SQL kimlik doğrulama kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="876c3-116">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="876c3-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="876c3-117">-AsJob</span></span>
<span data-ttu-id="876c3-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="876c3-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="876c3-119">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="876c3-119">-AssignIdentity</span></span>
<span data-ttu-id="876c3-120">Azure Keykasa gibi temel yönetim hizmetleriyle kullanılmak üzere bu yönetilen örnek için bir Azure Active Directory kimliği oluşturun ve atayın.</span><span class="sxs-lookup"><span data-stu-id="876c3-120">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="876c3-121">-Harmanlama</span><span class="sxs-lookup"><span data-stu-id="876c3-121">-Collation</span></span>
<span data-ttu-id="876c3-122">Kullanılacak Azure SQL yönetilen örneğinin harmanlaması.</span><span class="sxs-lookup"><span data-stu-id="876c3-122">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="876c3-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="876c3-123">-ComputeGeneration</span></span>
<span data-ttu-id="876c3-124">Örnek için hesaplama oluşturma.</span><span class="sxs-lookup"><span data-stu-id="876c3-124">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="876c3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="876c3-125">-DefaultProfile</span></span>
<span data-ttu-id="876c3-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="876c3-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="876c3-127">-Edition</span><span class="sxs-lookup"><span data-stu-id="876c3-127">-Edition</span></span>
<span data-ttu-id="876c3-128">Örneğin sürümü.</span><span class="sxs-lookup"><span data-stu-id="876c3-128">The edition for the instance.</span></span>

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

### <span data-ttu-id="876c3-129">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="876c3-129">-LicenseType</span></span>
<span data-ttu-id="876c3-130">Hangi lisans türünün kullanılacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="876c3-130">Determines which License Type to use.</span></span> <span data-ttu-id="876c3-131">Olası değerler:</span><span class="sxs-lookup"><span data-stu-id="876c3-131">Possible values are:</span></span>
- <span data-ttu-id="876c3-132">Temel fiyat-Azure Karma avantajı (AHB) mevcut SQL Server lisans sahiplerinin indirimli fiyatlandırması uygulanır.</span><span class="sxs-lookup"><span data-stu-id="876c3-132">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="876c3-133">Yönetilen örnek hizmeti fiyatı var olan SQL Server lisans sahipleri için düşülecektir.</span><span class="sxs-lookup"><span data-stu-id="876c3-133">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="876c3-134">Licenseeklenmiş-Azure Karma avantajı (AHB) mevcut SQL Server lisans sahiplerinin indirim fiyatlandırması uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="876c3-134">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="876c3-135">Yönetilen örnek hizmeti fiyatı Yeni bir SQL Server lisans maliyetleri içerir.</span><span class="sxs-lookup"><span data-stu-id="876c3-135">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="876c3-136">-Konum</span><span class="sxs-lookup"><span data-stu-id="876c3-136">-Location</span></span>
<span data-ttu-id="876c3-137">Örneğin oluşturulacağı konum</span><span class="sxs-lookup"><span data-stu-id="876c3-137">The location in which to create the instance</span></span>

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

### <span data-ttu-id="876c3-138">-Ad</span><span class="sxs-lookup"><span data-stu-id="876c3-138">-Name</span></span>
<span data-ttu-id="876c3-139">Örnek adı.</span><span class="sxs-lookup"><span data-stu-id="876c3-139">Instance name.</span></span>

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

### <span data-ttu-id="876c3-140">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="876c3-140">-ProxyOverride</span></span>
<span data-ttu-id="876c3-141">Örneğe bağlanmak için kullanılan bağlantı türü.</span><span class="sxs-lookup"><span data-stu-id="876c3-141">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="876c3-142">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="876c3-142">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="876c3-143">Örnek için genel veri uç noktasının etkinleştirilip etkinleştirilmediğini.</span><span class="sxs-lookup"><span data-stu-id="876c3-143">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="876c3-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="876c3-144">-ResourceGroupName</span></span>
<span data-ttu-id="876c3-145">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="876c3-145">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="876c3-146">-SkuName</span><span class="sxs-lookup"><span data-stu-id="876c3-146">-SkuName</span></span>
<span data-ttu-id="876c3-147">Örneğin ' GP_Gen4 ', ' BC_Gen4 ' örnek adı.</span><span class="sxs-lookup"><span data-stu-id="876c3-147">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="876c3-148">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="876c3-148">-StorageSizeInGB</span></span>
<span data-ttu-id="876c3-149">Örnekle ilişkilendirilecek depolama boyutu miktarını belirler</span><span class="sxs-lookup"><span data-stu-id="876c3-149">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="876c3-150">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="876c3-150">-SubnetId</span></span>
<span data-ttu-id="876c3-151">Örnek oluşturma için kullanılacak alt ağ kimliği</span><span class="sxs-lookup"><span data-stu-id="876c3-151">The Subnet Id to use for instance creation</span></span>

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

### <span data-ttu-id="876c3-152">Etiketli</span><span class="sxs-lookup"><span data-stu-id="876c3-152">-Tag</span></span>
<span data-ttu-id="876c3-153">Örnekle ilişkilendirilecek Etiketler</span><span class="sxs-lookup"><span data-stu-id="876c3-153">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="876c3-154">-TimeZoneId</span><span class="sxs-lookup"><span data-stu-id="876c3-154">-TimezoneId</span></span>
<span data-ttu-id="876c3-155">Ayarlanacak örnek için saat dilimi kimliği.</span><span class="sxs-lookup"><span data-stu-id="876c3-155">The time zone id for the instance to set.</span></span> <span data-ttu-id="876c3-156">Saat dilimi kimliklerinin listesi sys.time_zone_info (Transact-SQL) görünümünde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="876c3-156">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="876c3-157">-VCore</span><span class="sxs-lookup"><span data-stu-id="876c3-157">-VCore</span></span>
<span data-ttu-id="876c3-158">Örnekle ne kadar Vçekirdeğin ilişkilendiyeceğini belirler</span><span class="sxs-lookup"><span data-stu-id="876c3-158">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="876c3-159">-Onay</span><span class="sxs-lookup"><span data-stu-id="876c3-159">-Confirm</span></span>
<span data-ttu-id="876c3-160">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="876c3-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="876c3-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="876c3-161">-WhatIf</span></span>
<span data-ttu-id="876c3-162">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="876c3-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="876c3-163">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="876c3-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="876c3-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="876c3-164">CommonParameters</span></span>
<span data-ttu-id="876c3-165">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="876c3-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="876c3-166">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="876c3-166">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="876c3-167">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="876c3-167">INPUTS</span></span>

### <span data-ttu-id="876c3-168">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="876c3-168">None</span></span>

## <span data-ttu-id="876c3-169">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="876c3-169">OUTPUTS</span></span>

### <span data-ttu-id="876c3-170">Microsoft. Azure. Commands. Sql. ManagedInstance. model. Azureskalite Managedınstancemodel</span><span class="sxs-lookup"><span data-stu-id="876c3-170">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="876c3-171">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="876c3-171">NOTES</span></span>

## <span data-ttu-id="876c3-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="876c3-172">RELATED LINKS</span></span>
