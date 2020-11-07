---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: c08d2b1a08e76603af7125d0d4671643133699da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933761"
---
# <span data-ttu-id="5cc4b-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5cc4b-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="5cc4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cc4b-102">SYNOPSIS</span></span>
<span data-ttu-id="5cc4b-103">Azure SQL veritabanı yönetilen örneğinin özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="5cc4b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5cc4b-104">SYNTAX</span></span>

### <span data-ttu-id="5cc4b-105">Setınstancefrominınputparameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5cc4b-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5cc4b-106">Setınstancefrolauressqlmanagedınstancemodelınstancedefinition</span><span class="sxs-lookup"><span data-stu-id="5cc4b-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5cc4b-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="5cc4b-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cc4b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5cc4b-108">DESCRIPTION</span></span>
<span data-ttu-id="5cc4b-109">**Set-Azsqlınstance** cmdlet 'ı, Azure SQL veritabanı yönetilen örneğinin özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="5cc4b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5cc4b-110">EXAMPLES</span></span>

### <span data-ttu-id="5cc4b-111">Örnek 1: yeni değer-\Administrators parolası kullanarak var olan örneği ayarla,-LicenseType,-StorageSizeInGB ve-VCore</span><span class="sxs-lookup"><span data-stu-id="5cc4b-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>
```powershell
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16
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

<span data-ttu-id="5cc4b-112">Bu komut,-\Administrators parolası,-LicenseType,-StorageSizeInGB ve-VCore kullanarak var olan örneği ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-112">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="5cc4b-113">Örnek 2: örnek havuzundaki bir örnek için yeni-\Administrators parolası,-LicenseType,-StorageSizeInGB ve-VCore değerlerini kullanarak varolan örneği ayarlayın</span><span class="sxs-lookup"><span data-stu-id="5cc4b-113">Example 2: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
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

<span data-ttu-id="5cc4b-114">Bu komut, örnek havuzundaki bir örnek için yeni-\Administrators parolası,-LicenseType,-StorageSizeInGB ve-VCore değerlerini kullanarak var olan örneği ayarlar</span><span class="sxs-lookup"><span data-stu-id="5cc4b-114">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

## <span data-ttu-id="5cc4b-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5cc4b-115">PARAMETERS</span></span>

### <span data-ttu-id="5cc4b-116">-\Administrators parolası</span><span class="sxs-lookup"><span data-stu-id="5cc4b-116">-AdministratorPassword</span></span>
<span data-ttu-id="5cc4b-117">Örnek için yeni SQL Yöneticisi parolası.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-117">The new SQL administrator password for the instance.</span></span>

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

### <span data-ttu-id="5cc4b-118">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="5cc4b-118">-AssignIdentity</span></span>
<span data-ttu-id="5cc4b-119">Azure Keykasa gibi temel yönetim hizmetleriyle kullanılmak üzere bu örnek için bir Azure Active Directory kimliği oluşturun ve atayın.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-119">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="5cc4b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cc4b-120">-DefaultProfile</span></span>
<span data-ttu-id="5cc4b-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cc4b-122">-Edition</span><span class="sxs-lookup"><span data-stu-id="5cc4b-122">-Edition</span></span>
<span data-ttu-id="5cc4b-123">Örneğe atanacak sürüm.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-123">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="5cc4b-124">-Force</span><span class="sxs-lookup"><span data-stu-id="5cc4b-124">-Force</span></span>
<span data-ttu-id="5cc4b-125">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="5cc4b-125">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="5cc4b-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5cc4b-126">-InputObject</span></span>
<span data-ttu-id="5cc4b-127">Kaldırılacak Azurestabmanagedınstancemodel nesnesi</span><span class="sxs-lookup"><span data-stu-id="5cc4b-127">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="5cc4b-128">-Instancepoolname</span><span class="sxs-lookup"><span data-stu-id="5cc4b-128">-InstancePoolName</span></span>
<span data-ttu-id="5cc4b-129">Örnek havuz adı.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-129">The instance pool name.</span></span>

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

### <span data-ttu-id="5cc4b-130">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5cc4b-130">-LicenseType</span></span>
<span data-ttu-id="5cc4b-131">Hangi lisans türünün kullanılacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-131">Determines which License Type to use.</span></span> <span data-ttu-id="5cc4b-132">Olası değerler:</span><span class="sxs-lookup"><span data-stu-id="5cc4b-132">Possible values are:</span></span>
- <span data-ttu-id="5cc4b-133">Temel fiyat-Azure Karma avantajı (AHB) mevcut SQL Server lisans sahiplerinin indirimli fiyatlandırması uygulanır.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-133">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="5cc4b-134">Yönetilen örnek hizmeti fiyatı var olan SQL Server lisans sahipleri için düşülecektir.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-134">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="5cc4b-135">Licenseeklenmiş-Azure Karma avantajı (AHB) mevcut SQL Server lisans sahiplerinin indirim fiyatlandırması uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-135">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="5cc4b-136">Yönetilen örnek hizmeti fiyatı Yeni bir SQL Server lisans maliyetleri içerir.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-136">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="5cc4b-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="5cc4b-137">-Name</span></span>
<span data-ttu-id="5cc4b-138">Örnek adı.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-138">Instance name.</span></span>

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

### <span data-ttu-id="5cc4b-139">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="5cc4b-139">-ProxyOverride</span></span>
<span data-ttu-id="5cc4b-140">Örneğe bağlanmak için kullanılan bağlantı türü.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-140">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="5cc4b-141">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="5cc4b-141">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="5cc4b-142">Örnek için genel veri uç noktasının etkinleştirilip etkinleştirilmediğini.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-142">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="5cc4b-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cc4b-143">-ResourceGroupName</span></span>
<span data-ttu-id="5cc4b-144">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="5cc4b-145">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5cc4b-145">-ResourceId</span></span>
<span data-ttu-id="5cc4b-146">Kaldırılacak örneğin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="5cc4b-146">The resource id of instance to remove</span></span>

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

### <span data-ttu-id="5cc4b-147">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="5cc4b-147">-StorageSizeInGB</span></span>
<span data-ttu-id="5cc4b-148">Örnekle ilişkilendirilecek depolama boyutu miktarını belirler</span><span class="sxs-lookup"><span data-stu-id="5cc4b-148">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="5cc4b-149">Etiketli</span><span class="sxs-lookup"><span data-stu-id="5cc4b-149">-Tag</span></span>
<span data-ttu-id="5cc4b-150">Örnekle ilişkilendirilecek Etiketler.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-150">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="5cc4b-151">-VCore</span><span class="sxs-lookup"><span data-stu-id="5cc4b-151">-VCore</span></span>
<span data-ttu-id="5cc4b-152">Örnekle ne kadar Vçekirdeğin ilişkilendiyeceğini belirler</span><span class="sxs-lookup"><span data-stu-id="5cc4b-152">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="5cc4b-153">-Onay</span><span class="sxs-lookup"><span data-stu-id="5cc4b-153">-Confirm</span></span>
<span data-ttu-id="5cc4b-154">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cc4b-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cc4b-155">-WhatIf</span></span>
<span data-ttu-id="5cc4b-156">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cc4b-157">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cc4b-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cc4b-158">CommonParameters</span></span>
<span data-ttu-id="5cc4b-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cc4b-160">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5cc4b-160">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cc4b-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5cc4b-161">INPUTS</span></span>

### <span data-ttu-id="5cc4b-162">Microsoft. Azure. Commands. Sql. ManagedInstance. model. Azureskalite Managedınstancemodel</span><span class="sxs-lookup"><span data-stu-id="5cc4b-162">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="5cc4b-163">System. String</span><span class="sxs-lookup"><span data-stu-id="5cc4b-163">System.String</span></span>

## <span data-ttu-id="5cc4b-164">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5cc4b-164">OUTPUTS</span></span>

### <span data-ttu-id="5cc4b-165">Microsoft. Azure. Commands. Sql. ManagedInstance. model. Azureskalite Managedınstancemodel</span><span class="sxs-lookup"><span data-stu-id="5cc4b-165">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="5cc4b-166">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5cc4b-166">NOTES</span></span>

## <span data-ttu-id="5cc4b-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5cc4b-167">RELATED LINKS</span></span>
