---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/update-azurermautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Update-AzureRmAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Update-AzureRmAutomationSourceControl.md
ms.openlocfilehash: 78308306e7bc46d4a9b3fadf4b00050cf9898f26
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763916"
---
# <span data-ttu-id="e7823-101">Update-AzureRmAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="e7823-101">Update-AzureRmAutomationSourceControl</span></span>

## <span data-ttu-id="e7823-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7823-102">SYNOPSIS</span></span>
<span data-ttu-id="e7823-103">Azure Otomasyonu kaynak denetimini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e7823-103">Updates an Azure Automation source control.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7823-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e7823-104">SYNTAX</span></span>

```
Update-AzureRmAutomationSourceControl -Name <String> [-AccessToken <SecureString>] [-FolderPath <String>]
 [-Branch <String>] [-Description <String>] [-AutoSync <Boolean>] [-PublishRunbook <Boolean>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7823-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7823-105">DESCRIPTION</span></span>
<span data-ttu-id="e7823-106">Update-AzureRmAutomationSourceControl cmdlet 'i, Azure Otomasyonu 'nda kaynak denetimindeki bir alanın değerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e7823-106">The Update-AzureRmAutomationSourceControl cmdlet modifies the value of a field in a source control in Azure Automation.</span></span>

## <span data-ttu-id="e7823-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e7823-107">EXAMPLES</span></span>

### <span data-ttu-id="e7823-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e7823-108">Example 1</span></span>
<span data-ttu-id="e7823-109">Bu komutlar, Devrunbook alanını, Devsnative adlı hesap adındaki VSTSNative için false olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e7823-109">This commands sets the PublishRunbook field to false for the Azure Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
Update-AzureRmAutomationSourceControl -ResourceGroupName "rg1" `
                                      -AutomationAccountName "devAccount" `
                                      -Name "VSTSNative" `
                                      -PublishRunbook $false 

Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    False          https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="e7823-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e7823-110">PARAMETERS</span></span>

### <span data-ttu-id="e7823-111">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="e7823-111">-AccessToken</span></span>
<span data-ttu-id="e7823-112">Kaynak denetimi erişim belirteci.</span><span class="sxs-lookup"><span data-stu-id="e7823-112">The source control access token.</span></span>

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

### <span data-ttu-id="e7823-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e7823-113">-AutomationAccountName</span></span>
<span data-ttu-id="e7823-114">Otomasyon hesap adı.</span><span class="sxs-lookup"><span data-stu-id="e7823-114">The automation account name.</span></span>

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

### <span data-ttu-id="e7823-115">-AutoSync</span><span class="sxs-lookup"><span data-stu-id="e7823-115">-AutoSync</span></span>
<span data-ttu-id="e7823-116">Kaynak denetimin autoSync özelliği.</span><span class="sxs-lookup"><span data-stu-id="e7823-116">The autoSync property for the source control.</span></span>

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

### <span data-ttu-id="e7823-117">-Dal</span><span class="sxs-lookup"><span data-stu-id="e7823-117">-Branch</span></span>
<span data-ttu-id="e7823-118">Kaynak denetim dalı.</span><span class="sxs-lookup"><span data-stu-id="e7823-118">The source control branch.</span></span>

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

### <span data-ttu-id="e7823-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7823-119">-DefaultProfile</span></span>
<span data-ttu-id="e7823-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e7823-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7823-121">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="e7823-121">-Description</span></span>
<span data-ttu-id="e7823-122">Kaynak denetimi açıklaması.</span><span class="sxs-lookup"><span data-stu-id="e7823-122">The source control description.</span></span>

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

### <span data-ttu-id="e7823-123">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="e7823-123">-FolderPath</span></span>
<span data-ttu-id="e7823-124">Kaynak denetimi klasör yolu.</span><span class="sxs-lookup"><span data-stu-id="e7823-124">The source control folder path.</span></span>

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

### <span data-ttu-id="e7823-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="e7823-125">-Name</span></span>
<span data-ttu-id="e7823-126">Kaynak denetimi adı.</span><span class="sxs-lookup"><span data-stu-id="e7823-126">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7823-127">-PublishRunbook</span><span class="sxs-lookup"><span data-stu-id="e7823-127">-PublishRunbook</span></span>
<span data-ttu-id="e7823-128">Kaynak denetiminin publishRunbook özelliği.</span><span class="sxs-lookup"><span data-stu-id="e7823-128">The publishRunbook property of the source control.</span></span>

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

### <span data-ttu-id="e7823-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7823-129">-ResourceGroupName</span></span>
<span data-ttu-id="e7823-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e7823-130">The resource group name.</span></span>

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

### <span data-ttu-id="e7823-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="e7823-131">-Confirm</span></span>
<span data-ttu-id="e7823-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e7823-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7823-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7823-133">-WhatIf</span></span>
<span data-ttu-id="e7823-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e7823-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7823-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e7823-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7823-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7823-136">CommonParameters</span></span>
<span data-ttu-id="e7823-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e7823-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7823-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7823-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7823-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e7823-139">INPUTS</span></span>

### <span data-ttu-id="e7823-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e7823-140">System.String</span></span>

## <span data-ttu-id="e7823-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e7823-141">OUTPUTS</span></span>

### <span data-ttu-id="e7823-142">Microsoft. Azure. Commands. Automation. model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="e7823-142">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="e7823-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e7823-143">NOTES</span></span>

## <span data-ttu-id="e7823-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e7823-144">RELATED LINKS</span></span>
