---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 0FF88136-4FC9-41F2-A3E6-BFADBAFF4E44
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/export-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRMAutomationRunbook.md
ms.openlocfilehash: 7bc8305c8b0d861398807f7eefae4a741f60cc52
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764732"
---
# <span data-ttu-id="b7d53-101">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b7d53-101">Export-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="b7d53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7d53-102">SYNOPSIS</span></span>
<span data-ttu-id="b7d53-103">Otomasyon Runbook 'unu dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="b7d53-103">Exports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7d53-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b7d53-104">SYNTAX</span></span>

```
Export-AzureRmAutomationRunbook [-Name] <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7d53-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b7d53-105">DESCRIPTION</span></span>
<span data-ttu-id="b7d53-106">**Export-AzureRmAutomationRunbook** cmdlet 'i, wps_2 veya Wps_2 iş akışı runbook 'ları için Wps_2 bir Azure Automation runbook 'unu (. ps1) bir</span><span class="sxs-lookup"><span data-stu-id="b7d53-106">The **Export-AzureRmAutomationRunbook** cmdlet exports an Azure Automation runbook to a wps_2 script (.ps1 ) file, for wps_2 or wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file, for graphical runbooks.</span></span>
<span data-ttu-id="b7d53-107">Runbook adı, verilen dosyanın adı olur.</span><span class="sxs-lookup"><span data-stu-id="b7d53-107">The name of the runbook becomes the name of the exported file.</span></span>

## <span data-ttu-id="b7d53-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b7d53-108">EXAMPLES</span></span>

### <span data-ttu-id="b7d53-109">Örnek 1: runbook dışarı aktarma</span><span class="sxs-lookup"><span data-stu-id="b7d53-109">Example 1: Export a runbook</span></span>
```
PS C:\>Export-AzureRmAutomationRunbook -ResourceGroupName "ResourceGroup01" -AutomationAccountName "ContosoAutomationAccount" -Name "Runbook03" -Slot "Published" -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="b7d53-110">Bu komut, bir Automation runbook 'un yayımlanmış sürümünü bir Kullanıcı masaüstüne aktarır.</span><span class="sxs-lookup"><span data-stu-id="b7d53-110">This command exports the published version of an Automation runbook to a user desktop.</span></span>

## <span data-ttu-id="b7d53-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b7d53-111">PARAMETERS</span></span>

### <span data-ttu-id="b7d53-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b7d53-112">-AutomationAccountName</span></span>
<span data-ttu-id="b7d53-113">Bu cmdlet 'in runbook dışarı aktardığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7d53-113">Specifies the name of the Automation account in which this cmdlet exports a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7d53-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7d53-114">-DefaultProfile</span></span>
<span data-ttu-id="b7d53-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b7d53-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7d53-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b7d53-116">-Force</span></span>
<span data-ttu-id="b7d53-117">ps_force</span><span class="sxs-lookup"><span data-stu-id="b7d53-117">ps_force</span></span>

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

### <span data-ttu-id="b7d53-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="b7d53-118">-Name</span></span>
<span data-ttu-id="b7d53-119">Bu cmdlet 'in dışarı aktardığı runbook adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7d53-119">Specifies the name of the runbook that this cmdlet exports.</span></span>
<span data-ttu-id="b7d53-120">Runbook adı, dışarı aktarma dosyasının adı olur.</span><span class="sxs-lookup"><span data-stu-id="b7d53-120">The name of the runbook becomes the name of the export file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7d53-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="b7d53-121">-OutputFolder</span></span>
<span data-ttu-id="b7d53-122">Bu cmdlet 'in dışarı aktarma dosyasını oluşturduğu klasörün yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7d53-122">Specifies the path of a folder in which this cmdlet creates the export file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7d53-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7d53-123">-ResourceGroupName</span></span>
<span data-ttu-id="b7d53-124">Bu cmdlet 'in runbook dışarı aktardığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7d53-124">Specifies the name of the resource group for which this cmdlet exports a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7d53-125">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="b7d53-125">-Slot</span></span>
<span data-ttu-id="b7d53-126">Bu cmdlet 'in runbook 'un taslak veya yayımlanmış içeriğini dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="b7d53-126">Specifies whether this cmdlet exports the draft or published content of the runbook.</span></span>
<span data-ttu-id="b7d53-127">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="b7d53-127">Valid values are:</span></span> 

- <span data-ttu-id="b7d53-128">Yayımlanabilir</span><span class="sxs-lookup"><span data-stu-id="b7d53-128">Published</span></span> 
- <span data-ttu-id="b7d53-129">Lar</span><span class="sxs-lookup"><span data-stu-id="b7d53-129">Draft</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7d53-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="b7d53-130">-Confirm</span></span>
<span data-ttu-id="b7d53-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b7d53-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7d53-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7d53-132">-WhatIf</span></span>
<span data-ttu-id="b7d53-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b7d53-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7d53-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b7d53-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7d53-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7d53-135">CommonParameters</span></span>
<span data-ttu-id="b7d53-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b7d53-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7d53-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7d53-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7d53-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b7d53-138">INPUTS</span></span>

### <span data-ttu-id="b7d53-139">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b7d53-139">None</span></span>
<span data-ttu-id="b7d53-140">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="b7d53-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b7d53-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b7d53-141">OUTPUTS</span></span>

### <span data-ttu-id="b7d53-142">System. ıO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="b7d53-142">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="b7d53-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b7d53-143">NOTES</span></span>

## <span data-ttu-id="b7d53-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b7d53-144">RELATED LINKS</span></span>

[<span data-ttu-id="b7d53-145">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b7d53-145">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="b7d53-146">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b7d53-146">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="b7d53-147">Yeni-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b7d53-147">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="b7d53-148">Yeni-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b7d53-148">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="b7d53-149">Yayımlama-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b7d53-149">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="b7d53-150">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b7d53-150">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="b7d53-151">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b7d53-151">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="b7d53-152">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b7d53-152">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


