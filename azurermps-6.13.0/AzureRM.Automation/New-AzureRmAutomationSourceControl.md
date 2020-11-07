---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationSourceControl.md
ms.openlocfilehash: d81d62e6ba391fb601817544d977f56e75522ba5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591445"
---
# <span data-ttu-id="1d12c-101">New-AzureRmAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="1d12c-101">New-AzureRmAutomationSourceControl</span></span>

## <span data-ttu-id="1d12c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d12c-102">SYNOPSIS</span></span>
<span data-ttu-id="1d12c-103">Otomasyon kaynak denetimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1d12c-103">Creates an A Automation source control.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d12c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1d12c-104">SYNTAX</span></span>

```
New-AzureRmAutomationSourceControl -Name <String> -RepoUrl <Uri> -SourceType <String>
 -AccessToken <SecureString> -FolderPath <String> [-Branch <String>] [-Description <String>] [-EnableAutoSync]
 [-DoNotPublishRunbook] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d12c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1d12c-105">DESCRIPTION</span></span>
<span data-ttu-id="1d12c-106">New-AzureRmAutomationSourceControl cmdlet, Azure Otomasyonu hesabımı VSTS TFVC, VSTS git veya GitHub 'my bağlantısı oluşturmak için bir yapılandırma oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1d12c-106">The New-AzureRmAutomationSourceControl cmdlet creates a configuration to link my Azure Automation account with my VSTS TFVC, VSTS Git or GitHub.</span></span>

## <span data-ttu-id="1d12c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1d12c-107">EXAMPLES</span></span>

### <span data-ttu-id="1d12c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1d12c-108">Example 1</span></span>
<span data-ttu-id="1d12c-109">Azure Otomasyonu hesabımı VSTS TFVC projenizle ilişkilendirmek için bir kaynak denetimi yapılandırması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1d12c-109">Create a source control configuration to link my Azure Automation account with my VSTS TFVC project.</span></span> <span data-ttu-id="1d12c-110">TFVC projelerinin dalları yoktur ve bu nedenle, Branch parametresi belirtilmez.</span><span class="sxs-lookup"><span data-stu-id="1d12c-110">TFVC projects do not have branches, and therefore, the Branch parameter is not specified.</span></span>

```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzureRmAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSNative" `
                                           -RepoUrl "https://contoso.visualstudio.com/ContosoProduction/_versionControl" `
                                           -SourceType "VsoTfvc" `
                                           -FolderPath "/Runbooks" `
                                           -AccessToken $accessToken

Name        SourceType Branch FolderPath AutoSync PublishRunbook RepoUrl
----        ---------- ------ ---------- -------- -------------- -------
VSTSNative  VsoTfvc            /Runbooks True     True           https://contoso.visualstudio.com/ContosoProduc...
```

### <span data-ttu-id="1d12c-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1d12c-111">Example 2</span></span>
<span data-ttu-id="1d12c-112">Azure Otomasyonu hesabımı VSTS git projenizle ilişkilendirmek için bir kaynak denetimi yapılandırması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1d12c-112">Create a source control configuration to link my Azure Automation account with my VSTS Git project.</span></span>


```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzureRmAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSGit" `
                                           -RepoUrl "https://contoso.visualstudio.com/_git/Finance" `
                                           -SourceType "VsoGit" `
                                           -Branch "Development" `
                                           -FolderPath "/" `
                                           -AccessToken $accessToken

Name    SourceType Branch      FolderPath AutoSync PublishRunbook RepoUrl
----    ---------- ------      ---------- -------- -------------- -------
VSTSGit VsoGit     Development /          True     True           https://contoso.visualstudio.com/_git/Finan...
```

### <span data-ttu-id="1d12c-113">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="1d12c-113">Example 3</span></span>
<span data-ttu-id="1d12c-114">Azure Otomasyonu hesabımı GitHub projeceğim ile bağlantılandırmak için bir kaynak denetimi yapılandırması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1d12c-114">Create a source control configuration to link my Azure Automation account with my GitHub project.</span></span>


```powershell
PS C:\> # GitHub access token
PS C:\> $token = "68b08011223aac8bdd3388913a44rrsaa84fdf"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzureRmAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "GitHub1" `
                                           -RepoUrl "https://github.com/Contoso/TestSourceControl.git" `
                                           -SourceType "GitHub" `
                                           -Branch "master" `
                                           -FolderPath "/Runbooks" `
                                           -AccessToken $accessToken

Name    SourceType Branch FolderPath AutoSync PublishRunbook RepoUrl
----    ---------- ------ ---------- -------- -------------- -------
GitHub1 GitHub     master /Runbooks  True     True           https://github.com/Contoso/TestSourceControl...
```

## <span data-ttu-id="1d12c-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1d12c-115">PARAMETERS</span></span>

### <span data-ttu-id="1d12c-116">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="1d12c-116">-AccessToken</span></span>
<span data-ttu-id="1d12c-117">Kaynak denetimi erişim belirteci.</span><span class="sxs-lookup"><span data-stu-id="1d12c-117">The source control access token.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d12c-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1d12c-118">-AutomationAccountName</span></span>
<span data-ttu-id="1d12c-119">Otomasyon hesap adı.</span><span class="sxs-lookup"><span data-stu-id="1d12c-119">The automation account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d12c-120">-Dal</span><span class="sxs-lookup"><span data-stu-id="1d12c-120">-Branch</span></span>
<span data-ttu-id="1d12c-121">Kaynak denetim dalı.</span><span class="sxs-lookup"><span data-stu-id="1d12c-121">The source control branch.</span></span>

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

### <span data-ttu-id="1d12c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d12c-122">-DefaultProfile</span></span>
<span data-ttu-id="1d12c-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1d12c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d12c-124">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="1d12c-124">-Description</span></span>
<span data-ttu-id="1d12c-125">Kaynak denetimi açıklaması.</span><span class="sxs-lookup"><span data-stu-id="1d12c-125">The source control description.</span></span>

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

### <span data-ttu-id="1d12c-126">-DoNotPublishRunbook</span><span class="sxs-lookup"><span data-stu-id="1d12c-126">-DoNotPublishRunbook</span></span>
<span data-ttu-id="1d12c-127">Kaynak denetiminin publishRunbook özelliği.</span><span class="sxs-lookup"><span data-stu-id="1d12c-127">The publishRunbook property of the source control.</span></span>
<span data-ttu-id="1d12c-128">DoNotPublishRunbook ayarlanmışsa, bu, Kullanıcı runbook 'ların ' taslak ' olarak aktarılacağı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="1d12c-128">If DoNotPublishRunbook is set, this means that user runbooks will be imported as 'Draft'.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d12c-129">-EnableAutoSync</span><span class="sxs-lookup"><span data-stu-id="1d12c-129">-EnableAutoSync</span></span>
<span data-ttu-id="1d12c-130">Kaynak denetimin autoSync özelliği.</span><span class="sxs-lookup"><span data-stu-id="1d12c-130">The autoSync property for the source control.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d12c-131">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="1d12c-131">-FolderPath</span></span>
<span data-ttu-id="1d12c-132">Kaynak denetimi klasör yolu.</span><span class="sxs-lookup"><span data-stu-id="1d12c-132">The source control folder path.</span></span>

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

### <span data-ttu-id="1d12c-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="1d12c-133">-Name</span></span>
<span data-ttu-id="1d12c-134">Kaynak denetimi adı.</span><span class="sxs-lookup"><span data-stu-id="1d12c-134">The source control name.</span></span>

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

### <span data-ttu-id="1d12c-135">-RepoUrl</span><span class="sxs-lookup"><span data-stu-id="1d12c-135">-RepoUrl</span></span>
<span data-ttu-id="1d12c-136">Kaynak denetimi depo URL 'si.</span><span class="sxs-lookup"><span data-stu-id="1d12c-136">The source control repo url.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d12c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d12c-137">-ResourceGroupName</span></span>
<span data-ttu-id="1d12c-138">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1d12c-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d12c-139">-SourceType</span><span class="sxs-lookup"><span data-stu-id="1d12c-139">-SourceType</span></span>
<span data-ttu-id="1d12c-140">Kaynak Denetim türü.</span><span class="sxs-lookup"><span data-stu-id="1d12c-140">The source control type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GitHub, VsoGit, VsoTfvc

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d12c-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="1d12c-141">-Confirm</span></span>
<span data-ttu-id="1d12c-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1d12c-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d12c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d12c-143">-WhatIf</span></span>
<span data-ttu-id="1d12c-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1d12c-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d12c-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1d12c-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d12c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d12c-146">CommonParameters</span></span>
<span data-ttu-id="1d12c-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1d12c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d12c-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d12c-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d12c-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1d12c-149">INPUTS</span></span>

### <span data-ttu-id="1d12c-150">System. String</span><span class="sxs-lookup"><span data-stu-id="1d12c-150">System.String</span></span>

## <span data-ttu-id="1d12c-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1d12c-151">OUTPUTS</span></span>

### <span data-ttu-id="1d12c-152">Microsoft. Azure. Commands. Automation. model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="1d12c-152">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="1d12c-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1d12c-153">NOTES</span></span>

## <span data-ttu-id="1d12c-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1d12c-154">RELATED LINKS</span></span>