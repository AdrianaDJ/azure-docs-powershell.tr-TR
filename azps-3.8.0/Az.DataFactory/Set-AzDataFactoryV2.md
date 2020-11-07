---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
ms.openlocfilehash: 219e5b18a04332d2ee840fb41b92aa9d282a1792
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938303"
---
# <span data-ttu-id="07bc3-101">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="07bc3-101">Set-AzDataFactoryV2</span></span>

## <span data-ttu-id="07bc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07bc3-102">SYNOPSIS</span></span>
<span data-ttu-id="07bc3-103">Veri fabrikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="07bc3-103">Creates a data factory.</span></span>

## <span data-ttu-id="07bc3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="07bc3-104">SYNTAX</span></span>

### <span data-ttu-id="07bc3-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="07bc3-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07bc3-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="07bc3-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07bc3-107">ByResourceIdFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="07bc3-107">ByResourceIdFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07bc3-108">ByResourceIdFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="07bc3-108">ByResourceIdFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="07bc3-109">ByFactoryNameFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="07bc3-109">ByFactoryNameFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="07bc3-110">ByFactoryNameFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="07bc3-110">ByFactoryNameFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07bc3-111">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="07bc3-111">ByInputObject</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07bc3-112">ByInputObjectFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="07bc3-112">ByInputObjectFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07bc3-113">ByInputObjectFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="07bc3-113">ByInputObjectFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="07bc3-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="07bc3-114">DESCRIPTION</span></span>
<span data-ttu-id="07bc3-115">**Set-AzDataFactoryV2** cmdlet 'i belirtilen kaynak grubu adı ve konumuyla bir veri fabrikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="07bc3-115">The **Set-AzDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="07bc3-116">Bu işlemleri aşağıdaki sırada gerçekleştirin:--Veri Fabrikası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="07bc3-116">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="07bc3-117">--Bağlantılı hizmetler oluşturun.</span><span class="sxs-lookup"><span data-stu-id="07bc3-117">-- Create linked services.</span></span>
<span data-ttu-id="07bc3-118">--Veri kümeleri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="07bc3-118">-- Create datasets.</span></span>
<span data-ttu-id="07bc3-119">--Ardışık düzen oluşturun.</span><span class="sxs-lookup"><span data-stu-id="07bc3-119">-- Create a pipeline.</span></span>

## <span data-ttu-id="07bc3-120">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="07bc3-120">EXAMPLES</span></span>

### <span data-ttu-id="07bc3-121">Örnek 1: Veri Fabrikası oluşturma</span><span class="sxs-lookup"><span data-stu-id="07bc3-121">Example 1: Create a data factory</span></span>
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

### <span data-ttu-id="07bc3-122">Örnek 2: var olan bir fabrika nesnesini kullanarak repo yapılandırma ayrıntılarını içeren bir veri fabrikası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="07bc3-122">Example 2: Create a data factory with repo configuration details using an existing factory object.</span></span>
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

<span data-ttu-id="07bc3-123">Bu komut, Azure Deviops kaynak denetimi yapılandırması ile EastUS konumunda Obkiadf adlı bir veri fabrikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="07bc3-123">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with Azure DevOps source control configuration.</span></span>

### <span data-ttu-id="07bc3-124">Örnek 3: yeni bir fabrika nesnesi kullanarak GitHub repo yapılandırma ayrıntılarını içeren bir veri fabrikası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="07bc3-124">Example 3: Create a data factory with GitHub repo configuration details using a new factory object.</span></span>
```
PS C:\> New-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Location 'EastUS' -HostName 'https://github.com' -AccountName msdata -RepositoryName ADFRepo -CollaborationBranch master -RootFolder /

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
    RepoConfiguration : Microsoft.Azure.Management.DataFactory.Models.FactoryGitHubConfiguration
```

<span data-ttu-id="07bc3-125">Bu komut, GitHub Kaynak denetimi yapılandırması ile EastUS konumunda OBKIADF adlı bir veri fabrikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="07bc3-125">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with GitHub source control configuration..</span></span>

## <span data-ttu-id="07bc3-126">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="07bc3-126">PARAMETERS</span></span>

### <span data-ttu-id="07bc3-127">-AccountName</span><span class="sxs-lookup"><span data-stu-id="07bc3-127">-AccountName</span></span>
<span data-ttu-id="07bc3-128">Repo yapılandırması için hesap adı.</span><span class="sxs-lookup"><span data-stu-id="07bc3-128">The account name for repo configuration.</span></span>

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

### <span data-ttu-id="07bc3-129">-Işbirationbranch</span><span class="sxs-lookup"><span data-stu-id="07bc3-129">-CollaborationBranch</span></span>
<span data-ttu-id="07bc3-130">Repo yapılandırması için işbirliği dalı.</span><span class="sxs-lookup"><span data-stu-id="07bc3-130">The collaboration branch for repo configuration.</span></span>

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

### <span data-ttu-id="07bc3-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07bc3-131">-DefaultProfile</span></span>
<span data-ttu-id="07bc3-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="07bc3-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07bc3-133">-Force</span><span class="sxs-lookup"><span data-stu-id="07bc3-133">-Force</span></span>
<span data-ttu-id="07bc3-134">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="07bc3-134">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="07bc3-135">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="07bc3-135">-HostName</span></span>
<span data-ttu-id="07bc3-136">GitHub repo yapılandırması için ana bilgisayar adı.</span><span class="sxs-lookup"><span data-stu-id="07bc3-136">The host name for GitHub repo configuration.</span></span>

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

### <span data-ttu-id="07bc3-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07bc3-137">-InputObject</span></span>
<span data-ttu-id="07bc3-138">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="07bc3-138">The data factory object.</span></span>

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

### <span data-ttu-id="07bc3-139">-Lastcommid</span><span class="sxs-lookup"><span data-stu-id="07bc3-139">-LastCommitId</span></span>
<span data-ttu-id="07bc3-140">Repo yapılandırması için son kayıt kimliği.</span><span class="sxs-lookup"><span data-stu-id="07bc3-140">The last commit id for repo configuration.</span></span>

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

### <span data-ttu-id="07bc3-141">-Konum</span><span class="sxs-lookup"><span data-stu-id="07bc3-141">-Location</span></span>
<span data-ttu-id="07bc3-142">Veri Fabrikası bu bölgede oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="07bc3-142">The data factory is created in this region.</span></span>

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

### <span data-ttu-id="07bc3-143">-Ad</span><span class="sxs-lookup"><span data-stu-id="07bc3-143">-Name</span></span>
<span data-ttu-id="07bc3-144">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="07bc3-144">The data factory name.</span></span>

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

### <span data-ttu-id="07bc3-145">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="07bc3-145">-ProjectName</span></span>
<span data-ttu-id="07bc3-146">Repo yapılandırması için proje adı Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="07bc3-146">The project name Azure DevOps for repo configuration.</span></span>

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

### <span data-ttu-id="07bc3-147">-Bir ad</span><span class="sxs-lookup"><span data-stu-id="07bc3-147">-RepositoryName</span></span>
<span data-ttu-id="07bc3-148">Repo yapılandırması için depo adı.</span><span class="sxs-lookup"><span data-stu-id="07bc3-148">The repository name for repo configuration.</span></span>

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

### <span data-ttu-id="07bc3-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07bc3-149">-ResourceGroupName</span></span>
<span data-ttu-id="07bc3-150">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="07bc3-150">The resource group name.</span></span>

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

### <span data-ttu-id="07bc3-151">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="07bc3-151">-ResourceId</span></span>
<span data-ttu-id="07bc3-152">V2 Data Factory 'in Azure Resource ID 'si.</span><span class="sxs-lookup"><span data-stu-id="07bc3-152">The Azure resource ID of V2 data factory.</span></span>

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

### <span data-ttu-id="07bc3-153">-RootFolder</span><span class="sxs-lookup"><span data-stu-id="07bc3-153">-RootFolder</span></span>
<span data-ttu-id="07bc3-154">Repo yapılandırması için kök klasörü.</span><span class="sxs-lookup"><span data-stu-id="07bc3-154">The root folder for repo configuration.</span></span>

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

### <span data-ttu-id="07bc3-155">Etiketli</span><span class="sxs-lookup"><span data-stu-id="07bc3-155">-Tag</span></span>
<span data-ttu-id="07bc3-156">Veri Fabrikası 'nin etiketleri.</span><span class="sxs-lookup"><span data-stu-id="07bc3-156">The tags of the data factory.</span></span>

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

### <span data-ttu-id="07bc3-157">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="07bc3-157">-TenantId</span></span>
<span data-ttu-id="07bc3-158">Azure DevOps refpo yapılandırması için Kiracı kimliği.</span><span class="sxs-lookup"><span data-stu-id="07bc3-158">The tenant id for Azure DevOps repo configuration.</span></span>

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

### <span data-ttu-id="07bc3-159">-Onay</span><span class="sxs-lookup"><span data-stu-id="07bc3-159">-Confirm</span></span>
<span data-ttu-id="07bc3-160">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="07bc3-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07bc3-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07bc3-161">-WhatIf</span></span>
<span data-ttu-id="07bc3-162">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="07bc3-162">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="07bc3-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07bc3-163">CommonParameters</span></span>
<span data-ttu-id="07bc3-164">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="07bc3-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07bc3-165">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07bc3-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07bc3-166">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="07bc3-166">INPUTS</span></span>

### <span data-ttu-id="07bc3-167">System. String</span><span class="sxs-lookup"><span data-stu-id="07bc3-167">System.String</span></span>

### <span data-ttu-id="07bc3-168">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="07bc3-168">System.Collections.Hashtable</span></span>

## <span data-ttu-id="07bc3-169">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="07bc3-169">OUTPUTS</span></span>

### <span data-ttu-id="07bc3-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="07bc3-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="07bc3-171">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="07bc3-171">NOTES</span></span>
<span data-ttu-id="07bc3-172">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="07bc3-172">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="07bc3-173">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="07bc3-173">RELATED LINKS</span></span>

[<span data-ttu-id="07bc3-174">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="07bc3-174">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="07bc3-175">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="07bc3-175">Remove-AzDataFactoryV2</span></span>]()
