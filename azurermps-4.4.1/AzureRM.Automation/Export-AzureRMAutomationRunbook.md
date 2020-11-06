---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 0FF88136-4FC9-41F2-A3E6-BFADBAFF4E44
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRMAutomationRunbook.md
ms.openlocfilehash: b78b992e74252f645faabcf284c817b1cb3c1d5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587007"
---
# <span data-ttu-id="a01b4-101">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a01b4-101">Export-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="a01b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a01b4-102">SYNOPSIS</span></span>
<span data-ttu-id="a01b4-103">Otomasyon Runbook 'unu dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="a01b4-103">Exports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a01b4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a01b4-104">SYNTAX</span></span>

```
Export-AzureRmAutomationRunbook [-Name] <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a01b4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a01b4-105">DESCRIPTION</span></span>
<span data-ttu-id="a01b4-106">**Export-AzureRmAutomationRunbook** cmdlet 'i, wps_2 veya Wps_2 iş akışı runbook 'ları için Wps_2 bir Azure Automation runbook 'unu (. ps1) bir</span><span class="sxs-lookup"><span data-stu-id="a01b4-106">The **Export-AzureRmAutomationRunbook** cmdlet exports an Azure Automation runbook to a wps_2 script (.ps1 ) file, for wps_2 or wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file, for graphical runbooks.</span></span>
<span data-ttu-id="a01b4-107">Runbook adı, verilen dosyanın adı olur.</span><span class="sxs-lookup"><span data-stu-id="a01b4-107">The name of the runbook becomes the name of the exported file.</span></span>

## <span data-ttu-id="a01b4-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a01b4-108">EXAMPLES</span></span>

### <span data-ttu-id="a01b4-109">Örnek 1: runbook dışarı aktarma</span><span class="sxs-lookup"><span data-stu-id="a01b4-109">Example 1: Export a runbook</span></span>
```
PS C:\>Export-AzureRmAutomationRunbook -ResourceGroupName "ResourceGroup01" -AutomationAccountName "ContosoAutomationAccount" -Name "Runbook03" -Slot "Published" -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="a01b4-110">Bu komut, bir Automation runbook 'un yayımlanmış sürümünü bir Kullanıcı masaüstüne aktarır.</span><span class="sxs-lookup"><span data-stu-id="a01b4-110">This command exports the published version of an Automation runbook to a user desktop.</span></span>

## <span data-ttu-id="a01b4-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a01b4-111">PARAMETERS</span></span>

### <span data-ttu-id="a01b4-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a01b4-112">-AutomationAccountName</span></span>
<span data-ttu-id="a01b4-113">Bu cmdlet 'in runbook dışarı aktardığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a01b4-113">Specifies the name of the Automation account in which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="a01b4-114">-Force</span><span class="sxs-lookup"><span data-stu-id="a01b4-114">-Force</span></span>
<span data-ttu-id="a01b4-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="a01b4-115">ps_force</span></span>

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

### <span data-ttu-id="a01b4-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="a01b4-116">-Name</span></span>
<span data-ttu-id="a01b4-117">Bu cmdlet 'in dışarı aktardığı runbook adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a01b4-117">Specifies the name of the runbook that this cmdlet exports.</span></span>
<span data-ttu-id="a01b4-118">Runbook adı, dışarı aktarma dosyasının adı olur.</span><span class="sxs-lookup"><span data-stu-id="a01b4-118">The name of the runbook becomes the name of the export file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a01b4-119">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="a01b4-119">-OutputFolder</span></span>
<span data-ttu-id="a01b4-120">Bu cmdlet 'in dışarı aktarma dosyasını oluşturduğu klasörün yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a01b4-120">Specifies the path of a folder in which this cmdlet creates the export file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a01b4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a01b4-121">-ResourceGroupName</span></span>
<span data-ttu-id="a01b4-122">Bu cmdlet 'in runbook dışarı aktardığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a01b4-122">Specifies the name of the resource group for which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="a01b4-123">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="a01b4-123">-Slot</span></span>
<span data-ttu-id="a01b4-124">Bu cmdlet 'in runbook 'un taslak veya yayımlanmış içeriğini dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="a01b4-124">Specifies whether this cmdlet exports the draft or published content of the runbook.</span></span>
<span data-ttu-id="a01b4-125">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="a01b4-125">Valid values are:</span></span> 

- <span data-ttu-id="a01b4-126">Yayımlanabilir</span><span class="sxs-lookup"><span data-stu-id="a01b4-126">Published</span></span> 
- <span data-ttu-id="a01b4-127">Lar</span><span class="sxs-lookup"><span data-stu-id="a01b4-127">Draft</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01b4-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="a01b4-128">-Confirm</span></span>
<span data-ttu-id="a01b4-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a01b4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a01b4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a01b4-130">-WhatIf</span></span>
<span data-ttu-id="a01b4-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a01b4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a01b4-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a01b4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a01b4-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a01b4-133">-DefaultProfile</span></span>
<span data-ttu-id="a01b4-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a01b4-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a01b4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a01b4-135">CommonParameters</span></span>
<span data-ttu-id="a01b4-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a01b4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a01b4-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a01b4-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a01b4-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a01b4-138">INPUTS</span></span>

## <span data-ttu-id="a01b4-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a01b4-139">OUTPUTS</span></span>

### <span data-ttu-id="a01b4-140">System. ıO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="a01b4-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="a01b4-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a01b4-141">NOTES</span></span>

## <span data-ttu-id="a01b4-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a01b4-142">RELATED LINKS</span></span>

[<span data-ttu-id="a01b4-143">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a01b4-143">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="a01b4-144">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a01b4-144">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="a01b4-145">Yeni-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a01b4-145">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="a01b4-146">Yeni-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a01b4-146">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="a01b4-147">Yayımlama-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a01b4-147">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="a01b4-148">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a01b4-148">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="a01b4-149">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a01b4-149">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="a01b4-150">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a01b4-150">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


