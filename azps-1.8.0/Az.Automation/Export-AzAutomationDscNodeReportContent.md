---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 4285EF77-FA70-4BE7-96E0-89E2E8FC5AD6
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationdscnodereportcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
ms.openlocfilehash: 6d9abefee1f787ea26f7f10b106900af0be31d3c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761642"
---
# <span data-ttu-id="89fb8-101">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="89fb8-101">Export-AzAutomationDscNodeReportContent</span></span>

## <span data-ttu-id="89fb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89fb8-102">SYNOPSIS</span></span>
<span data-ttu-id="89fb8-103">DSC düğümünden Otomasyon 'a gönderilen bir DSC raporunun ham içeriğini dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="89fb8-103">Exports the raw content of a DSC report sent from a DSC node to Automation.</span></span>

## <span data-ttu-id="89fb8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="89fb8-104">SYNTAX</span></span>

```
Export-AzAutomationDscNodeReportContent -NodeId <Guid> -ReportId <Guid> [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89fb8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="89fb8-105">DESCRIPTION</span></span>
<span data-ttu-id="89fb8-106">**Export-AzAutomationDscNodeReportContent** cmdlet 'ı, APS Istenen durum yapılandırma (DSC) raporunun ham içeriğini dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="89fb8-106">The **Export-AzAutomationDscNodeReportContent** cmdlet exports the raw contents of an APS Desired State Configuration (DSC) report.</span></span>
<span data-ttu-id="89fb8-107">DSC düğümü, Azure Otomasyonu 'na bir DSC raporu gönderir.</span><span class="sxs-lookup"><span data-stu-id="89fb8-107">A DSC node sends a DSC report to Azure Automation.</span></span>

## <span data-ttu-id="89fb8-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="89fb8-108">EXAMPLES</span></span>

### <span data-ttu-id="89fb8-109">Örnek 1: DSC düğümünden rapor dışarı aktarma</span><span class="sxs-lookup"><span data-stu-id="89fb8-109">Example 1: Export a report from a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "AutomationAccount01" -Name "Computer14"
PS C:\> $Report = Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "ContosoAutomationAccount" -NodeId $Node.Id -Latest
PS C:\> $Report | Export-AzAutomationDscNodeReportContent -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="89fb8-110">Bu komut kümesi, Computer14 adlı DSC düğümünden masaüstüne en son raporu dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="89fb8-110">This set of commands exports the latest report from the DSC node named Computer14 to the desktop.</span></span>

## <span data-ttu-id="89fb8-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="89fb8-111">PARAMETERS</span></span>

### <span data-ttu-id="89fb8-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="89fb8-112">-AutomationAccountName</span></span>
<span data-ttu-id="89fb8-113">Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="89fb8-113">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="89fb8-114">Bu cmdlet, bu parametrenin belirttiği Otomasyon hesabına ait bir DSC düğümünün rapor içeriğini dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="89fb8-114">This cmdlet exports report content for a DSC node that belongs to the Automation account that this parameter specifies.</span></span>

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

### <span data-ttu-id="89fb8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89fb8-115">-DefaultProfile</span></span>
<span data-ttu-id="89fb8-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="89fb8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89fb8-117">-Force</span><span class="sxs-lookup"><span data-stu-id="89fb8-117">-Force</span></span>
<span data-ttu-id="89fb8-118">Bu cmdlet 'in varolan bir yerel dosyayı aynı ada sahip yeni bir dosyayla değiştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="89fb8-118">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="89fb8-119">-NodeId</span><span class="sxs-lookup"><span data-stu-id="89fb8-119">-NodeId</span></span>
<span data-ttu-id="89fb8-120">Bu cmdlet 'in rapor içeriğini dışarı aktardığı DSC düğümünün benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="89fb8-120">Specifies the unique ID of the DSC node for which this cmdlet exports report contents.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89fb8-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="89fb8-121">-OutputFolder</span></span>
<span data-ttu-id="89fb8-122">Bu cmdlet 'in rapor içeriğini dışarı aktardığı çıkış klasörünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="89fb8-122">Specifies the output folder where this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="89fb8-123">-ReportId</span><span class="sxs-lookup"><span data-stu-id="89fb8-123">-ReportId</span></span>
<span data-ttu-id="89fb8-124">Bu cmdlet 'in dışarı aktardığı DSC düğümü raporunun benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="89fb8-124">Specifies the unique ID of the DSC node report that this cmdlet exports.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89fb8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89fb8-125">-ResourceGroupName</span></span>
<span data-ttu-id="89fb8-126">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="89fb8-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="89fb8-127">Bu cmdlet, bu cmdlet 'in belirttiği kaynak grubuna ait DSC düğümünün içeriğini dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="89fb8-127">This cmdlet exports the contents of a report for the DSC node that belongs to the resource group that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="89fb8-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="89fb8-128">-Confirm</span></span>
<span data-ttu-id="89fb8-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="89fb8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89fb8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89fb8-130">-WhatIf</span></span>
<span data-ttu-id="89fb8-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="89fb8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89fb8-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="89fb8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89fb8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89fb8-133">CommonParameters</span></span>
<span data-ttu-id="89fb8-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="89fb8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89fb8-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89fb8-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89fb8-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="89fb8-136">INPUTS</span></span>

### <span data-ttu-id="89fb8-137">System. Guid</span><span class="sxs-lookup"><span data-stu-id="89fb8-137">System.Guid</span></span>

### <span data-ttu-id="89fb8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="89fb8-138">System.String</span></span>

## <span data-ttu-id="89fb8-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="89fb8-139">OUTPUTS</span></span>

### <span data-ttu-id="89fb8-140">System. ıO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="89fb8-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="89fb8-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="89fb8-141">NOTES</span></span>

## <span data-ttu-id="89fb8-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="89fb8-142">RELATED LINKS</span></span>

[<span data-ttu-id="89fb8-143">Dışarı aktarma-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="89fb8-143">Export-AzAutomationDscNodeReportContent</span></span>](./Export-AzAutomationDscNodeReportContent.md)

[<span data-ttu-id="89fb8-144">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="89fb8-144">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="89fb8-145">Get-AzAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="89fb8-145">Get-AzAutomationDscNodeReport</span></span>](./Get-AzAutomationDscNodeReport.md)


