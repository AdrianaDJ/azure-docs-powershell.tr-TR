---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: e17c6b226f7ed4fe17842c93d03828d53c0bb22c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266781"
---
# <span data-ttu-id="e62ae-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e62ae-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="e62ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e62ae-102">SYNOPSIS</span></span>
<span data-ttu-id="e62ae-103">Azure SQL veritabanı yönetilen örneğinin özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e62ae-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="e62ae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e62ae-104">SYNTAX</span></span>

### <span data-ttu-id="e62ae-105">Setınstancefrominınputparameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e62ae-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e62ae-106">Setınstancefrolauressqlmanagedınstancemodelınstancedefinition</span><span class="sxs-lookup"><span data-stu-id="e62ae-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e62ae-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="e62ae-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>]
 [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e62ae-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e62ae-108">DESCRIPTION</span></span>
<span data-ttu-id="e62ae-109">**Set-Azsqlınstance** cmdlet 'ı, Azure SQL veritabanı yönetilen örneğinin özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e62ae-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="e62ae-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e62ae-110">EXAMPLES</span></span>

### <span data-ttu-id="e62ae-111">Örnek 1: yeni,-\Administrators parolasının (-LicenseType,-StorageSizeInGB,-VCore ve-Edition)</span><span class="sxs-lookup"><span data-stu-id="e62ae-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore and -Edition</span></span>
```powershell
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -Edition BusinessCritical
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
InstancePoolName         :
```

### <span data-ttu-id="e62ae-112">Örnek 2: yeni değer için yeni değer kullanarak var olan örnek donanım üretimini ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="e62ae-112">Example 2: Change existing instance hardware generation using new value for -ComputeGeneration</span></span>
```powershell
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -ComputeGeneration Gen5
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
InstancePoolName         :
```

<span data-ttu-id="e62ae-113">Bu komut,-\Administrators parolası,-LicenseType,-StorageSizeInGB ve-VCore kullanarak var olan örneği ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e62ae-113">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="e62ae-114">Örnek 3: örnek havuzundaki bir örnek için yeni-\Administrators parolası,-LicenseType,-StorageSizeInGB ve-VCore değerlerini kullanarak varolan örneği ayarlayın</span><span class="sxs-lookup"><span data-stu-id="e62ae-114">Example 3: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
```powershell
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 2 -InstancePoolName instancePool0
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
StorageSizeInGB          : 1024
InstancePoolName         : instancePool0
```

<span data-ttu-id="e62ae-115">Bu komut, örnek havuzundaki bir örnek için yeni-\Administrators parolası,-LicenseType,-StorageSizeInGB ve-VCore değerlerini kullanarak var olan örneği ayarlar</span><span class="sxs-lookup"><span data-stu-id="e62ae-115">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

## <span data-ttu-id="e62ae-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e62ae-116">PARAMETERS</span></span>

### <span data-ttu-id="e62ae-117">-\Administrators parolası</span><span class="sxs-lookup"><span data-stu-id="e62ae-117">-AdministratorPassword</span></span>
<span data-ttu-id="e62ae-118">Örnek için yeni SQL Yöneticisi parolası.</span><span class="sxs-lookup"><span data-stu-id="e62ae-118">The new SQL administrator password for the instance.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62ae-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="e62ae-119">-AsJob</span></span>
<span data-ttu-id="e62ae-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e62ae-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e62ae-121">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="e62ae-121">-AssignIdentity</span></span>
<span data-ttu-id="e62ae-122">Azure Keykasa gibi temel yönetim hizmetleriyle kullanılmak üzere bu örnek için bir Azure Active Directory kimliği oluşturun ve atayın.</span><span class="sxs-lookup"><span data-stu-id="e62ae-122">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="e62ae-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="e62ae-123">-ComputeGeneration</span></span>
<span data-ttu-id="e62ae-124">Örnek için hesaplama oluşturma.</span><span class="sxs-lookup"><span data-stu-id="e62ae-124">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="e62ae-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e62ae-125">-DefaultProfile</span></span>
<span data-ttu-id="e62ae-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e62ae-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e62ae-127">-Edition</span><span class="sxs-lookup"><span data-stu-id="e62ae-127">-Edition</span></span>
<span data-ttu-id="e62ae-128">Örneğe atanacak sürüm.</span><span class="sxs-lookup"><span data-stu-id="e62ae-128">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="e62ae-129">-Force</span><span class="sxs-lookup"><span data-stu-id="e62ae-129">-Force</span></span>
<span data-ttu-id="e62ae-130">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="e62ae-130">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="e62ae-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e62ae-131">-InputObject</span></span>
<span data-ttu-id="e62ae-132">Kaldırılacak Azurestabmanagedınstancemodel nesnesi</span><span class="sxs-lookup"><span data-stu-id="e62ae-132">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e62ae-133">-Instancepoolname</span><span class="sxs-lookup"><span data-stu-id="e62ae-133">-InstancePoolName</span></span>
<span data-ttu-id="e62ae-134">Örnek havuz adı.</span><span class="sxs-lookup"><span data-stu-id="e62ae-134">The instance pool name.</span></span>

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

### <span data-ttu-id="e62ae-135">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="e62ae-135">-LicenseType</span></span>
<span data-ttu-id="e62ae-136">Hangi lisans türünün kullanılacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="e62ae-136">Determines which License Type to use.</span></span> <span data-ttu-id="e62ae-137">Olası değerler:</span><span class="sxs-lookup"><span data-stu-id="e62ae-137">Possible values are:</span></span>
- <span data-ttu-id="e62ae-138">Temel fiyat-Azure Karma avantajı (AHB) mevcut SQL Server lisans sahiplerinin indirimli fiyatlandırması uygulanır.</span><span class="sxs-lookup"><span data-stu-id="e62ae-138">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="e62ae-139">Yönetilen örnek hizmeti fiyatı var olan SQL Server lisans sahipleri için düşülecektir.</span><span class="sxs-lookup"><span data-stu-id="e62ae-139">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="e62ae-140">Licenseeklenmiş-Azure Karma avantajı (AHB) mevcut SQL Server lisans sahiplerinin indirim fiyatlandırması uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="e62ae-140">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="e62ae-141">Yönetilen örnek hizmeti fiyatı Yeni bir SQL Server lisans maliyetleri içerir.</span><span class="sxs-lookup"><span data-stu-id="e62ae-141">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="e62ae-142">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="e62ae-142">-MinimalTlsVersion</span></span>
<span data-ttu-id="e62ae-143">Yönetilen örneğe uygulanacak en az TLS sürümü</span><span class="sxs-lookup"><span data-stu-id="e62ae-143">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="e62ae-144">-Ad</span><span class="sxs-lookup"><span data-stu-id="e62ae-144">-Name</span></span>
<span data-ttu-id="e62ae-145">Örnek adı.</span><span class="sxs-lookup"><span data-stu-id="e62ae-145">Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62ae-146">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="e62ae-146">-ProxyOverride</span></span>
<span data-ttu-id="e62ae-147">Örneğe bağlanmak için kullanılan bağlantı türü.</span><span class="sxs-lookup"><span data-stu-id="e62ae-147">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="e62ae-148">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="e62ae-148">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="e62ae-149">Örnek için genel veri uç noktasının etkinleştirilip etkinleştirilmediğini.</span><span class="sxs-lookup"><span data-stu-id="e62ae-149">Whether or not the public data endpoint is enabled for the instance.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62ae-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e62ae-150">-ResourceGroupName</span></span>
<span data-ttu-id="e62ae-151">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e62ae-151">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62ae-152">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e62ae-152">-ResourceId</span></span>
<span data-ttu-id="e62ae-153">Kaldırılacak örneğin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="e62ae-153">The resource id of instance to remove</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e62ae-154">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="e62ae-154">-StorageSizeInGB</span></span>
<span data-ttu-id="e62ae-155">Örnekle ilişkilendirilecek depolama boyutu miktarını belirler</span><span class="sxs-lookup"><span data-stu-id="e62ae-155">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62ae-156">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e62ae-156">-Tag</span></span>
<span data-ttu-id="e62ae-157">Örnekle ilişkilendirilecek Etiketler.</span><span class="sxs-lookup"><span data-stu-id="e62ae-157">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="e62ae-158">-VCore</span><span class="sxs-lookup"><span data-stu-id="e62ae-158">-VCore</span></span>
<span data-ttu-id="e62ae-159">Örnekle ne kadar Vçekirdeğin ilişkilendiyeceğini belirler</span><span class="sxs-lookup"><span data-stu-id="e62ae-159">Determines how much VCore to associate with instance</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62ae-160">-Onay</span><span class="sxs-lookup"><span data-stu-id="e62ae-160">-Confirm</span></span>
<span data-ttu-id="e62ae-161">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e62ae-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e62ae-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e62ae-162">-WhatIf</span></span>
<span data-ttu-id="e62ae-163">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e62ae-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e62ae-164">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e62ae-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e62ae-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e62ae-165">CommonParameters</span></span>
<span data-ttu-id="e62ae-166">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e62ae-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e62ae-167">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e62ae-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e62ae-168">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e62ae-168">INPUTS</span></span>

### <span data-ttu-id="e62ae-169">Microsoft. Azure. Commands. Sql. ManagedInstance. model. Azureskalite Managedınstancemodel</span><span class="sxs-lookup"><span data-stu-id="e62ae-169">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="e62ae-170">System. String</span><span class="sxs-lookup"><span data-stu-id="e62ae-170">System.String</span></span>

## <span data-ttu-id="e62ae-171">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e62ae-171">OUTPUTS</span></span>

### <span data-ttu-id="e62ae-172">Microsoft. Azure. Commands. Sql. ManagedInstance. model. Azureskalite Managedınstancemodel</span><span class="sxs-lookup"><span data-stu-id="e62ae-172">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="e62ae-173">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e62ae-173">NOTES</span></span>

## <span data-ttu-id="e62ae-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e62ae-174">RELATED LINKS</span></span>
