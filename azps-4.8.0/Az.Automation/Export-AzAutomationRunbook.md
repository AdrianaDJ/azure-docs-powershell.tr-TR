---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 0FF88136-4FC9-41F2-A3E6-BFADBAFF4E44
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
ms.openlocfilehash: 03a57c35063a401aa5f730e11538532bdbbbc58c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107971"
---
# <span data-ttu-id="0d70c-101">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0d70c-101">Export-AzAutomationRunbook</span></span>

## <span data-ttu-id="0d70c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d70c-102">SYNOPSIS</span></span>
<span data-ttu-id="0d70c-103">Otomasyon Runbook 'unu dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="0d70c-103">Exports an Automation runbook.</span></span>

## <span data-ttu-id="0d70c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0d70c-104">SYNTAX</span></span>

```
Export-AzAutomationRunbook [-Name] <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d70c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0d70c-105">DESCRIPTION</span></span>
<span data-ttu-id="0d70c-106">**Export-AzAutomationRunbook** cmdlet 'i, wps_2 veya Wps_2 iş akışı runbook 'ları için Wps_2 bir Azure Otomasyonu runbook 'u veya grafik runbook 'lar için bir grafik runbook (. graphrunbook) dosyasını dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="0d70c-106">The **Export-AzAutomationRunbook** cmdlet exports an Azure Automation runbook to a wps_2 script (.ps1 ) file, for wps_2 or wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file, for graphical runbooks.</span></span>
<span data-ttu-id="0d70c-107">Runbook adı, verilen dosyanın adı olur.</span><span class="sxs-lookup"><span data-stu-id="0d70c-107">The name of the runbook becomes the name of the exported file.</span></span>

## <span data-ttu-id="0d70c-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0d70c-108">EXAMPLES</span></span>

### <span data-ttu-id="0d70c-109">Örnek 1: runbook dışarı aktarma</span><span class="sxs-lookup"><span data-stu-id="0d70c-109">Example 1: Export a runbook</span></span>
```
PS C:\>Export-AzAutomationRunbook -ResourceGroupName "ResourceGroup01" -AutomationAccountName "ContosoAutomationAccount" -Name "Runbook03" -Slot "Published" -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="0d70c-110">Bu komut, bir Automation runbook 'un yayımlanmış sürümünü bir Kullanıcı masaüstüne aktarır.</span><span class="sxs-lookup"><span data-stu-id="0d70c-110">This command exports the published version of an Automation runbook to a user desktop.</span></span>

## <span data-ttu-id="0d70c-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0d70c-111">PARAMETERS</span></span>

### <span data-ttu-id="0d70c-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0d70c-112">-AutomationAccountName</span></span>
<span data-ttu-id="0d70c-113">Bu cmdlet 'in runbook dışarı aktardığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d70c-113">Specifies the name of the Automation account in which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="0d70c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d70c-114">-DefaultProfile</span></span>
<span data-ttu-id="0d70c-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0d70c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d70c-116">-Force</span><span class="sxs-lookup"><span data-stu-id="0d70c-116">-Force</span></span>
<span data-ttu-id="0d70c-117">ps_force</span><span class="sxs-lookup"><span data-stu-id="0d70c-117">ps_force</span></span>

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

### <span data-ttu-id="0d70c-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="0d70c-118">-Name</span></span>
<span data-ttu-id="0d70c-119">Bu cmdlet 'in dışarı aktardığı runbook adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d70c-119">Specifies the name of the runbook that this cmdlet exports.</span></span>
<span data-ttu-id="0d70c-120">Runbook adı, dışarı aktarma dosyasının adı olur.</span><span class="sxs-lookup"><span data-stu-id="0d70c-120">The name of the runbook becomes the name of the export file.</span></span>

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

### <span data-ttu-id="0d70c-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="0d70c-121">-OutputFolder</span></span>
<span data-ttu-id="0d70c-122">Bu cmdlet 'in dışarı aktarma dosyasını oluşturduğu klasörün yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d70c-122">Specifies the path of a folder in which this cmdlet creates the export file.</span></span>

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

### <span data-ttu-id="0d70c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d70c-123">-ResourceGroupName</span></span>
<span data-ttu-id="0d70c-124">Bu cmdlet 'in runbook dışarı aktardığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d70c-124">Specifies the name of the resource group for which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="0d70c-125">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="0d70c-125">-Slot</span></span>
<span data-ttu-id="0d70c-126">Bu cmdlet 'in runbook 'un taslak veya yayımlanmış içeriğini dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="0d70c-126">Specifies whether this cmdlet exports the draft or published content of the runbook.</span></span>
<span data-ttu-id="0d70c-127">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="0d70c-127">Valid values are:</span></span> 
- <span data-ttu-id="0d70c-128">Yayımlanabilir</span><span class="sxs-lookup"><span data-stu-id="0d70c-128">Published</span></span> 
- <span data-ttu-id="0d70c-129">Lar</span><span class="sxs-lookup"><span data-stu-id="0d70c-129">Draft</span></span>

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

### <span data-ttu-id="0d70c-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="0d70c-130">-Confirm</span></span>
<span data-ttu-id="0d70c-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0d70c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d70c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d70c-132">-WhatIf</span></span>
<span data-ttu-id="0d70c-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0d70c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d70c-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0d70c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d70c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d70c-135">CommonParameters</span></span>
<span data-ttu-id="0d70c-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0d70c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d70c-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d70c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d70c-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0d70c-138">INPUTS</span></span>

### <span data-ttu-id="0d70c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0d70c-139">System.String</span></span>

## <span data-ttu-id="0d70c-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0d70c-140">OUTPUTS</span></span>

### <span data-ttu-id="0d70c-141">System. ıO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="0d70c-141">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="0d70c-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0d70c-142">NOTES</span></span>

## <span data-ttu-id="0d70c-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0d70c-143">RELATED LINKS</span></span>

[<span data-ttu-id="0d70c-144">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0d70c-144">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="0d70c-145">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0d70c-145">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="0d70c-146">Yeni-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0d70c-146">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="0d70c-147">Yeni-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0d70c-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="0d70c-148">Yayımlama-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0d70c-148">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="0d70c-149">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0d70c-149">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="0d70c-150">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0d70c-150">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="0d70c-151">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0d70c-151">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


