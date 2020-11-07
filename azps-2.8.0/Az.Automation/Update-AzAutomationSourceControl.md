---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/update-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Update-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Update-AzAutomationSourceControl.md
ms.openlocfilehash: 7786431232f9570557593d2fbdde65a21e34f9bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753187"
---
# <span data-ttu-id="041ff-101">Update-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="041ff-101">Update-AzAutomationSourceControl</span></span>

## <span data-ttu-id="041ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="041ff-102">SYNOPSIS</span></span>
<span data-ttu-id="041ff-103">Azure Otomasyonu kaynak denetimini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="041ff-103">Updates an Azure Automation source control.</span></span>

## <span data-ttu-id="041ff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="041ff-104">SYNTAX</span></span>

```
Update-AzAutomationSourceControl -Name <String> [-AccessToken <SecureString>] [-FolderPath <String>]
 [-Branch <String>] [-Description <String>] [-AutoSync <Boolean>] [-PublishRunbook <Boolean>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="041ff-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="041ff-105">DESCRIPTION</span></span>
<span data-ttu-id="041ff-106">Update-AzAutomationSourceControl cmdlet 'i, Azure Otomasyonu 'nda kaynak denetimindeki bir alanın değerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="041ff-106">The Update-AzAutomationSourceControl cmdlet modifies the value of a field in a source control in Azure Automation.</span></span>

## <span data-ttu-id="041ff-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="041ff-107">EXAMPLES</span></span>

### <span data-ttu-id="041ff-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="041ff-108">Example 1</span></span>
<span data-ttu-id="041ff-109">Bu komutlar, Devrunbook alanını, Devsnative adlı hesap adındaki VSTSNative için false olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="041ff-109">This commands sets the PublishRunbook field to false for the Azure Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
Update-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                      -AutomationAccountName "devAccount" `
                                      -Name "VSTSNative" `
                                      -PublishRunbook $false 

Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    False          https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="041ff-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="041ff-110">PARAMETERS</span></span>

### <span data-ttu-id="041ff-111">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="041ff-111">-AccessToken</span></span>
<span data-ttu-id="041ff-112">Kaynak denetimi erişim belirteci.</span><span class="sxs-lookup"><span data-stu-id="041ff-112">The source control access token.</span></span>

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

### <span data-ttu-id="041ff-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="041ff-113">-AutomationAccountName</span></span>
<span data-ttu-id="041ff-114">Otomasyon hesap adı.</span><span class="sxs-lookup"><span data-stu-id="041ff-114">The automation account name.</span></span>

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

### <span data-ttu-id="041ff-115">-AutoSync</span><span class="sxs-lookup"><span data-stu-id="041ff-115">-AutoSync</span></span>
<span data-ttu-id="041ff-116">Kaynak denetimin autoSync özelliği.</span><span class="sxs-lookup"><span data-stu-id="041ff-116">The autoSync property for the source control.</span></span>

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

### <span data-ttu-id="041ff-117">-Dal</span><span class="sxs-lookup"><span data-stu-id="041ff-117">-Branch</span></span>
<span data-ttu-id="041ff-118">Kaynak denetim dalı.</span><span class="sxs-lookup"><span data-stu-id="041ff-118">The source control branch.</span></span>

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

### <span data-ttu-id="041ff-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="041ff-119">-DefaultProfile</span></span>
<span data-ttu-id="041ff-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="041ff-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="041ff-121">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="041ff-121">-Description</span></span>
<span data-ttu-id="041ff-122">Kaynak denetimi açıklaması.</span><span class="sxs-lookup"><span data-stu-id="041ff-122">The source control description.</span></span>

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

### <span data-ttu-id="041ff-123">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="041ff-123">-FolderPath</span></span>
<span data-ttu-id="041ff-124">Kaynak denetimi klasör yolu.</span><span class="sxs-lookup"><span data-stu-id="041ff-124">The source control folder path.</span></span>

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

### <span data-ttu-id="041ff-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="041ff-125">-Name</span></span>
<span data-ttu-id="041ff-126">Kaynak denetimi adı.</span><span class="sxs-lookup"><span data-stu-id="041ff-126">The source control name.</span></span>

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

### <span data-ttu-id="041ff-127">-PublishRunbook</span><span class="sxs-lookup"><span data-stu-id="041ff-127">-PublishRunbook</span></span>
<span data-ttu-id="041ff-128">Kaynak denetiminin publishRunbook özelliği.</span><span class="sxs-lookup"><span data-stu-id="041ff-128">The publishRunbook property of the source control.</span></span>

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

### <span data-ttu-id="041ff-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="041ff-129">-ResourceGroupName</span></span>
<span data-ttu-id="041ff-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="041ff-130">The resource group name.</span></span>

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

### <span data-ttu-id="041ff-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="041ff-131">-Confirm</span></span>
<span data-ttu-id="041ff-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="041ff-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="041ff-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="041ff-133">-WhatIf</span></span>
<span data-ttu-id="041ff-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="041ff-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="041ff-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="041ff-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="041ff-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="041ff-136">CommonParameters</span></span>
<span data-ttu-id="041ff-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="041ff-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="041ff-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="041ff-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="041ff-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="041ff-139">INPUTS</span></span>

### <span data-ttu-id="041ff-140">System. String</span><span class="sxs-lookup"><span data-stu-id="041ff-140">System.String</span></span>

## <span data-ttu-id="041ff-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="041ff-141">OUTPUTS</span></span>

### <span data-ttu-id="041ff-142">Microsoft. Azure. Commands. Automation. model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="041ff-142">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="041ff-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="041ff-143">NOTES</span></span>

## <span data-ttu-id="041ff-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="041ff-144">RELATED LINKS</span></span>
