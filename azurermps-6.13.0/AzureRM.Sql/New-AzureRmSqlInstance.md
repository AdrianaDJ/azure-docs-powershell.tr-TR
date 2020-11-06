---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlInstance.md
ms.openlocfilehash: 025a9acc53405aeb1e211473b5f8f13066791714
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594343"
---
# <span data-ttu-id="044b8-101">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="044b8-101">New-AzureRmSqlInstance</span></span>

## <span data-ttu-id="044b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="044b8-102">SYNOPSIS</span></span>
<span data-ttu-id="044b8-103">Azure SQL veritabanı yönetilen örneği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="044b8-103">Creates an Azure SQL Database Managed Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="044b8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="044b8-104">SYNTAX</span></span>

### <span data-ttu-id="044b8-105">NewByEditionAndComputeGenerationParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="044b8-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Tag <Hashtable>] [-AssignIdentity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="044b8-106">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="044b8-106">NewBySkuNameParameterSetParameter</span></span>
```
New-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -SkuName <String> [-Tag <Hashtable>] [-AssignIdentity] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="044b8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="044b8-107">DESCRIPTION</span></span>
<span data-ttu-id="044b8-108">**New-Azurermsqlınstance** cmdlet 'ı BIR Azure SQL veritabanı yönetilen örneği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="044b8-108">The **New-AzureRmSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="044b8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="044b8-109">EXAMPLES</span></span>

### <span data-ttu-id="044b8-110">Örnek 1: yeni bir örnek oluşturma</span><span class="sxs-lookup"><span data-stu-id="044b8-110">Example 1: Create a new instance</span></span>
```
PS C:\>New-AzureRmSqlInstance -Name managedInstance1 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -SkuName GP_Gen4
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

<span data-ttu-id="044b8-111">Bu komut, sürüm ve ComputeGeneration parametrelerini kullanarak yeni bir örnek oluşturur.</span><span class="sxs-lookup"><span data-stu-id="044b8-111">This command creates a new instance by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="044b8-112">Örnek 2: yeni bir örnek oluşturma</span><span class="sxs-lookup"><span data-stu-id="044b8-112">Example 2: Create a new instance</span></span>
```
PS C:\>New-AzureRmSqlInstance -Name managedInstance2 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -Edition "GeneralPurpose" -ComputeGeneration Gen4
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

<span data-ttu-id="044b8-113">Bu komut, sürüm ve ComputeGeneration parametrelerini kullanarak yeni bir örnek oluşturur.</span><span class="sxs-lookup"><span data-stu-id="044b8-113">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

## <span data-ttu-id="044b8-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="044b8-114">PARAMETERS</span></span>

### <span data-ttu-id="044b8-115">-\Administrators kimlik bilgisi</span><span class="sxs-lookup"><span data-stu-id="044b8-115">-AdministratorCredential</span></span>
<span data-ttu-id="044b8-116">Örneğin SQL kimlik doğrulama kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="044b8-116">The SQL authentication credential of the instance.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="044b8-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="044b8-117">-AsJob</span></span>
<span data-ttu-id="044b8-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="044b8-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="044b8-119">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="044b8-119">-AssignIdentity</span></span>
<span data-ttu-id="044b8-120">Azure Keykasa gibi temel yönetim hizmetleriyle kullanılmak üzere bu yönetilen örnek için bir Azure Active Directory kimliği oluşturun ve atayın.</span><span class="sxs-lookup"><span data-stu-id="044b8-120">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="044b8-121">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="044b8-121">-ComputeGeneration</span></span>
<span data-ttu-id="044b8-122">Örnek için hesaplama oluşturma.</span><span class="sxs-lookup"><span data-stu-id="044b8-122">The compute generation for the instance.</span></span>

```yaml
Type: String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="044b8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="044b8-123">-DefaultProfile</span></span>
<span data-ttu-id="044b8-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="044b8-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="044b8-125">-Edition</span><span class="sxs-lookup"><span data-stu-id="044b8-125">-Edition</span></span>
<span data-ttu-id="044b8-126">Örneğin sürümü.</span><span class="sxs-lookup"><span data-stu-id="044b8-126">The edition for the instance.</span></span>

```yaml
Type: String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="044b8-127">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="044b8-127">-LicenseType</span></span>
<span data-ttu-id="044b8-128">Hangi tür kopyasının kullanılacağını belirler</span><span class="sxs-lookup"><span data-stu-id="044b8-128">Determines which License Type of instance to use</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="044b8-129">-Konum</span><span class="sxs-lookup"><span data-stu-id="044b8-129">-Location</span></span>
<span data-ttu-id="044b8-130">Örneğin oluşturulacağı konum</span><span class="sxs-lookup"><span data-stu-id="044b8-130">The location in which to create the instance</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="044b8-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="044b8-131">-Name</span></span>
<span data-ttu-id="044b8-132">Örnek adı.</span><span class="sxs-lookup"><span data-stu-id="044b8-132">Instance name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="044b8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="044b8-133">-ResourceGroupName</span></span>
<span data-ttu-id="044b8-134">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="044b8-134">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="044b8-135">-SkuName</span><span class="sxs-lookup"><span data-stu-id="044b8-135">-SkuName</span></span>
<span data-ttu-id="044b8-136">Örneğin ' GP_Gen4 ', ' BC_Gen4 ' örnek adı.</span><span class="sxs-lookup"><span data-stu-id="044b8-136">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

```yaml
Type: String
Parameter Sets: NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="044b8-137">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="044b8-137">-StorageSizeInGB</span></span>
<span data-ttu-id="044b8-138">Örnekle ilişkilendirilecek depolama boyutu miktarını belirler</span><span class="sxs-lookup"><span data-stu-id="044b8-138">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="044b8-139">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="044b8-139">-SubnetId</span></span>
<span data-ttu-id="044b8-140">Örnek oluşturma için kullanılacak alt ağ kimliği</span><span class="sxs-lookup"><span data-stu-id="044b8-140">The Subnet Id to use for instance creation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="044b8-141">Etiketli</span><span class="sxs-lookup"><span data-stu-id="044b8-141">-Tag</span></span>
<span data-ttu-id="044b8-142">Örnekle ilişkilendirilecek Etiketler</span><span class="sxs-lookup"><span data-stu-id="044b8-142">The tags to associate with the instance</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="044b8-143">-VCore</span><span class="sxs-lookup"><span data-stu-id="044b8-143">-VCore</span></span>
<span data-ttu-id="044b8-144">Örnekle ne kadar Vçekirdeğin ilişkilendiyeceğini belirler</span><span class="sxs-lookup"><span data-stu-id="044b8-144">Determines how much VCore to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="044b8-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="044b8-145">-Confirm</span></span>
<span data-ttu-id="044b8-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="044b8-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="044b8-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="044b8-147">-WhatIf</span></span>
<span data-ttu-id="044b8-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="044b8-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="044b8-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="044b8-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="044b8-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="044b8-150">CommonParameters</span></span>
<span data-ttu-id="044b8-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="044b8-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="044b8-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="044b8-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="044b8-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="044b8-153">INPUTS</span></span>

### <span data-ttu-id="044b8-154">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="044b8-154">None</span></span>

## <span data-ttu-id="044b8-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="044b8-155">OUTPUTS</span></span>

### <span data-ttu-id="044b8-156">Microsoft. Azure. Commands. Sql. ManagedInstance. model. Azureskalite Managedınstancemodel</span><span class="sxs-lookup"><span data-stu-id="044b8-156">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="044b8-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="044b8-157">NOTES</span></span>

## <span data-ttu-id="044b8-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="044b8-158">RELATED LINKS</span></span>
