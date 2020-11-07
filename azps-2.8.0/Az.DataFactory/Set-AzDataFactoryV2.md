---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
ms.openlocfilehash: 374263c26a3572e8d85e18d1795c27a761866a4a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752450"
---
# <span data-ttu-id="f9064-101">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f9064-101">Set-AzDataFactoryV2</span></span>

## <span data-ttu-id="f9064-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9064-102">SYNOPSIS</span></span>
<span data-ttu-id="f9064-103">Veri fabrikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f9064-103">Creates a data factory.</span></span>

## <span data-ttu-id="f9064-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f9064-104">SYNTAX</span></span>

### <span data-ttu-id="f9064-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f9064-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9064-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="f9064-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9064-107">ByResourceIdFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="f9064-107">ByResourceIdFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9064-108">ByResourceIdFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="f9064-108">ByResourceIdFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f9064-109">ByFactoryNameFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="f9064-109">ByFactoryNameFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f9064-110">ByFactoryNameFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="f9064-110">ByFactoryNameFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9064-111">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f9064-111">ByInputObject</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9064-112">ByInputObjectFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="f9064-112">ByInputObjectFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9064-113">ByInputObjectFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="f9064-113">ByInputObjectFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f9064-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="f9064-114">DESCRIPTION</span></span>
<span data-ttu-id="f9064-115">**Set-AzDataFactoryV2** cmdlet 'i belirtilen kaynak grubu adı ve konumuyla bir veri fabrikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f9064-115">The **Set-AzDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="f9064-116">Bu işlemleri aşağıdaki sırada gerçekleştirin:--Veri Fabrikası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f9064-116">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="f9064-117">--Bağlantılı hizmetler oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f9064-117">-- Create linked services.</span></span>
<span data-ttu-id="f9064-118">--Veri kümeleri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f9064-118">-- Create datasets.</span></span>
<span data-ttu-id="f9064-119">--Ardışık düzen oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f9064-119">-- Create a pipeline.</span></span>

## <span data-ttu-id="f9064-120">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f9064-120">EXAMPLES</span></span>

### <span data-ttu-id="f9064-121">Örnek 1: Veri Fabrikası oluşturma</span><span class="sxs-lookup"><span data-stu-id="f9064-121">Example 1: Create a data factory</span></span>
```
PS C:\> Set-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
    RepoConfiguration :
```

### <span data-ttu-id="f9064-122">Örnek 2: var olan bir fabrika nesnesini kullanarak repoconfiguration ayrıntılarını içeren bir veri fabrikası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f9064-122">Example 2: Create a data factory with repoconfiguration details using an existing factory object.</span></span>
```
PS C:\> Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" | Set-AzDataFactoryV2 -AccountName msdata -RepositoryName ADFRepo -CollaborationBranch master -RootFolder / -ProjectName "Azure Data Factory"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
    RepoConfiguration : Microsoft.Azure.Management.DataFactory.Models.FactoryVSTSConfiguration
```

<span data-ttu-id="f9064-123">Bu komut, WestUS konumunda ADF adlı kaynak grubunda WikiADF adlı bir veri fabrikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f9064-123">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="f9064-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f9064-124">PARAMETERS</span></span>

### <span data-ttu-id="f9064-125">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f9064-125">-AccountName</span></span>
<span data-ttu-id="f9064-126">Repo yapılandırması için hesap adı.</span><span class="sxs-lookup"><span data-stu-id="f9064-126">The account name for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9064-127">-Işbirationbranch</span><span class="sxs-lookup"><span data-stu-id="f9064-127">-CollaborationBranch</span></span>
<span data-ttu-id="f9064-128">Repo yapılandırması için işbirliği dalı.</span><span class="sxs-lookup"><span data-stu-id="f9064-128">The collaboration branch for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9064-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9064-129">-DefaultProfile</span></span>
<span data-ttu-id="f9064-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f9064-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9064-131">-Force</span><span class="sxs-lookup"><span data-stu-id="f9064-131">-Force</span></span>
<span data-ttu-id="f9064-132">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="f9064-132">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="f9064-133">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="f9064-133">-HostName</span></span>
<span data-ttu-id="f9064-134">Refpo yapılandırması için ana bilgisayar adı.</span><span class="sxs-lookup"><span data-stu-id="f9064-134">The host name for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9064-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9064-135">-InputObject</span></span>
<span data-ttu-id="f9064-136">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f9064-136">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByInputObject, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9064-137">-Lastcommid</span><span class="sxs-lookup"><span data-stu-id="f9064-137">-LastCommitId</span></span>
<span data-ttu-id="f9064-138">Repo yapılandırması için son kayıt kimliği.</span><span class="sxs-lookup"><span data-stu-id="f9064-138">The last commit id for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9064-139">-Konum</span><span class="sxs-lookup"><span data-stu-id="f9064-139">-Location</span></span>
<span data-ttu-id="f9064-140">Veri Fabrikası bu bölgede oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="f9064-140">The data factory is created in this region.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByResourceId, ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9064-141">-Ad</span><span class="sxs-lookup"><span data-stu-id="f9064-141">-Name</span></span>
<span data-ttu-id="f9064-142">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="f9064-142">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9064-143">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="f9064-143">-ProjectName</span></span>
<span data-ttu-id="f9064-144">Refpo yapılandırması için proje adı.</span><span class="sxs-lookup"><span data-stu-id="f9064-144">The project name for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByFactoryNameFactoryRepoVstsConfig, ByInputObjectFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9064-145">-Bir ad</span><span class="sxs-lookup"><span data-stu-id="f9064-145">-RepositoryName</span></span>
<span data-ttu-id="f9064-146">Repo yapılandırması için depo adı.</span><span class="sxs-lookup"><span data-stu-id="f9064-146">The repository name for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9064-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9064-147">-ResourceGroupName</span></span>
<span data-ttu-id="f9064-148">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f9064-148">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9064-149">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f9064-149">-ResourceId</span></span>
<span data-ttu-id="f9064-150">V2 Data Factory 'in Azure Resource ID 'si.</span><span class="sxs-lookup"><span data-stu-id="f9064-150">The Azure resource ID of V2 data factory.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId, ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig
Aliases: Id, DataFactoryId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9064-151">-RootFolder</span><span class="sxs-lookup"><span data-stu-id="f9064-151">-RootFolder</span></span>
<span data-ttu-id="f9064-152">Repo yapılandırması için kök klasörü.</span><span class="sxs-lookup"><span data-stu-id="f9064-152">The root folder for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9064-153">Etiketli</span><span class="sxs-lookup"><span data-stu-id="f9064-153">-Tag</span></span>
<span data-ttu-id="f9064-154">Veri Fabrikası 'nin etiketleri.</span><span class="sxs-lookup"><span data-stu-id="f9064-154">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByFactoryName, ByResourceId, ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByInputObject, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9064-155">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="f9064-155">-TenantId</span></span>
<span data-ttu-id="f9064-156">Repo yapılandırması için Kiracı kimliği.</span><span class="sxs-lookup"><span data-stu-id="f9064-156">The tenant id for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByFactoryNameFactoryRepoVstsConfig, ByInputObjectFactoryRepoVstsConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9064-157">-Onay</span><span class="sxs-lookup"><span data-stu-id="f9064-157">-Confirm</span></span>
<span data-ttu-id="f9064-158">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f9064-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9064-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9064-159">-WhatIf</span></span>
<span data-ttu-id="f9064-160">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="f9064-160">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="f9064-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9064-161">CommonParameters</span></span>
<span data-ttu-id="f9064-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f9064-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9064-163">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9064-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9064-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f9064-164">INPUTS</span></span>

### <span data-ttu-id="f9064-165">System. String</span><span class="sxs-lookup"><span data-stu-id="f9064-165">System.String</span></span>

### <span data-ttu-id="f9064-166">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f9064-166">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f9064-167">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f9064-167">OUTPUTS</span></span>

### <span data-ttu-id="f9064-168">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="f9064-168">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="f9064-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f9064-169">NOTES</span></span>
<span data-ttu-id="f9064-170">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="f9064-170">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f9064-171">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f9064-171">RELATED LINKS</span></span>

[<span data-ttu-id="f9064-172">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f9064-172">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="f9064-173">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f9064-173">Remove-AzDataFactoryV2</span></span>]()
