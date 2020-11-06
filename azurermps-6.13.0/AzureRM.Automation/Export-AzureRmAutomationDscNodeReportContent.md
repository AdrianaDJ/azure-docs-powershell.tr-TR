---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 4285EF77-FA70-4BE7-96E0-89E2E8FC5AD6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/export-azurermautomationdscnodereportcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscNodeReportContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscNodeReportContent.md
ms.openlocfilehash: 52ed2c5925758a4d40fdf39dcdadf73eb2fc53b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573017"
---
# <span data-ttu-id="df50e-101">Export-AzureRmAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="df50e-101">Export-AzureRmAutomationDscNodeReportContent</span></span>

## <span data-ttu-id="df50e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df50e-102">SYNOPSIS</span></span>
<span data-ttu-id="df50e-103">DSC düğümünden Otomasyon 'a gönderilen bir DSC raporunun ham içeriğini dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="df50e-103">Exports the raw content of a DSC report sent from a DSC node to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df50e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="df50e-104">SYNTAX</span></span>

```
Export-AzureRmAutomationDscNodeReportContent -NodeId <Guid> -ReportId <Guid> [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df50e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="df50e-105">DESCRIPTION</span></span>
<span data-ttu-id="df50e-106">**Export-AzureRmAutomationDscNodeReportContent** cmdlet 'ı, APS Istenen durum yapılandırma (DSC) raporunun ham içeriğini dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="df50e-106">The **Export-AzureRmAutomationDscNodeReportContent** cmdlet exports the raw contents of an APS Desired State Configuration (DSC) report.</span></span>
<span data-ttu-id="df50e-107">DSC düğümü, Azure Otomasyonu 'na bir DSC raporu gönderir.</span><span class="sxs-lookup"><span data-stu-id="df50e-107">A DSC node sends a DSC report to Azure Automation.</span></span>

## <span data-ttu-id="df50e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="df50e-108">EXAMPLES</span></span>

### <span data-ttu-id="df50e-109">Örnek 1: DSC düğümünden rapor dışarı aktarma</span><span class="sxs-lookup"><span data-stu-id="df50e-109">Example 1: Export a report from a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "AutomationAccount01" -Name "Computer14"
PS C:\> $Report = Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "ContosoAutomationAccount" -NodeId $Node.Id -Latest
PS C:\> $Report | Export-AzureRmAutomationDscNodeReportContent -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="df50e-110">Bu komut kümesi, Computer14 adlı DSC düğümünden masaüstüne en son raporu dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="df50e-110">This set of commands exports the latest report from the DSC node named Computer14 to the desktop.</span></span>

## <span data-ttu-id="df50e-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="df50e-111">PARAMETERS</span></span>

### <span data-ttu-id="df50e-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="df50e-112">-AutomationAccountName</span></span>
<span data-ttu-id="df50e-113">Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="df50e-113">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="df50e-114">Bu cmdlet, bu parametrenin belirttiği Otomasyon hesabına ait bir DSC düğümünün rapor içeriğini dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="df50e-114">This cmdlet exports report content for a DSC node that belongs to the Automation account that this parameter specifies.</span></span>

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

### <span data-ttu-id="df50e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df50e-115">-DefaultProfile</span></span>
<span data-ttu-id="df50e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="df50e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df50e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="df50e-117">-Force</span></span>
<span data-ttu-id="df50e-118">Bu cmdlet 'in varolan bir yerel dosyayı aynı ada sahip yeni bir dosyayla değiştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="df50e-118">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="df50e-119">-NodeId</span><span class="sxs-lookup"><span data-stu-id="df50e-119">-NodeId</span></span>
<span data-ttu-id="df50e-120">Bu cmdlet 'in rapor içeriğini dışarı aktardığı DSC düğümünün benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="df50e-120">Specifies the unique ID of the DSC node for which this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="df50e-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="df50e-121">-OutputFolder</span></span>
<span data-ttu-id="df50e-122">Bu cmdlet 'in rapor içeriğini dışarı aktardığı çıkış klasörünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="df50e-122">Specifies the output folder where this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="df50e-123">-ReportId</span><span class="sxs-lookup"><span data-stu-id="df50e-123">-ReportId</span></span>
<span data-ttu-id="df50e-124">Bu cmdlet 'in dışarı aktardığı DSC düğümü raporunun benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="df50e-124">Specifies the unique ID of the DSC node report that this cmdlet exports.</span></span>

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

### <span data-ttu-id="df50e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df50e-125">-ResourceGroupName</span></span>
<span data-ttu-id="df50e-126">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="df50e-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="df50e-127">Bu cmdlet, bu cmdlet 'in belirttiği kaynak grubuna ait DSC düğümünün içeriğini dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="df50e-127">This cmdlet exports the contents of a report for the DSC node that belongs to the resource group that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="df50e-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="df50e-128">-Confirm</span></span>
<span data-ttu-id="df50e-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="df50e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df50e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df50e-130">-WhatIf</span></span>
<span data-ttu-id="df50e-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="df50e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df50e-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="df50e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df50e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df50e-133">CommonParameters</span></span>
<span data-ttu-id="df50e-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="df50e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df50e-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df50e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df50e-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="df50e-136">INPUTS</span></span>

### <span data-ttu-id="df50e-137">System. Guid</span><span class="sxs-lookup"><span data-stu-id="df50e-137">System.Guid</span></span>

### <span data-ttu-id="df50e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="df50e-138">System.String</span></span>

## <span data-ttu-id="df50e-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="df50e-139">OUTPUTS</span></span>

### <span data-ttu-id="df50e-140">System. ıO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="df50e-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="df50e-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="df50e-141">NOTES</span></span>

## <span data-ttu-id="df50e-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="df50e-142">RELATED LINKS</span></span>

[<span data-ttu-id="df50e-143">Dışarı aktarma-AzureRmAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="df50e-143">Export-AzureRmAutomationDscNodeReportContent</span></span>](./Export-AzureRmAutomationDscNodeReportContent.md)

[<span data-ttu-id="df50e-144">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="df50e-144">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="df50e-145">Get-AzureRmAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="df50e-145">Get-AzureRmAutomationDscNodeReport</span></span>](./Get-AzureRmAutomationDscNodeReport.md)


