---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/publish-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
ms.openlocfilehash: e3d60cf277402ac23764b538ba6492ef5c424219
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591442"
---
# <span data-ttu-id="62395-101">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="62395-101">Publish-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="62395-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62395-102">SYNOPSIS</span></span>
<span data-ttu-id="62395-103">Runbook yayımlar.</span><span class="sxs-lookup"><span data-stu-id="62395-103">Publishes a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62395-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="62395-104">SYNTAX</span></span>

```
Publish-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62395-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="62395-105">DESCRIPTION</span></span>
<span data-ttu-id="62395-106">**Publish-AzureRmAutomationRunbook** cmdlet 'ı, Azure Otomasyonu 'nun üretim ortamında kullanılmak üzere bir runbook yayımlar.</span><span class="sxs-lookup"><span data-stu-id="62395-106">The **Publish-AzureRmAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="62395-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="62395-107">EXAMPLES</span></span>

### <span data-ttu-id="62395-108">Örnek 1: runbook yayımlama</span><span class="sxs-lookup"><span data-stu-id="62395-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="62395-109">Bu komut, Contoso17 adlı Azure Otomasyonu hesabında Runbk01 adındaki runbook 'u yayımlar.</span><span class="sxs-lookup"><span data-stu-id="62395-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="62395-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="62395-110">PARAMETERS</span></span>

### <span data-ttu-id="62395-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="62395-111">-AutomationAccountName</span></span>
<span data-ttu-id="62395-112">Bu cmdlet 'in runbook yayımladığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="62395-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="62395-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62395-113">-DefaultProfile</span></span>
<span data-ttu-id="62395-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="62395-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62395-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="62395-115">-Name</span></span>
<span data-ttu-id="62395-116">Bu cmdlet 'in yayımladığı runbook adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="62395-116">Specifies the name of the runbook that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="62395-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62395-117">-ResourceGroupName</span></span>
<span data-ttu-id="62395-118">Bu cmdlet 'in runbook yayımladığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="62395-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="62395-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62395-119">CommonParameters</span></span>
<span data-ttu-id="62395-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="62395-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62395-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62395-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62395-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="62395-122">INPUTS</span></span>

### <span data-ttu-id="62395-123">System. String</span><span class="sxs-lookup"><span data-stu-id="62395-123">System.String</span></span>

## <span data-ttu-id="62395-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="62395-124">OUTPUTS</span></span>

### <span data-ttu-id="62395-125">Microsoft. Azure. Commands. Automation. model. runbook</span><span class="sxs-lookup"><span data-stu-id="62395-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="62395-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="62395-126">NOTES</span></span>

## <span data-ttu-id="62395-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="62395-127">RELATED LINKS</span></span>

[<span data-ttu-id="62395-128">Dışarı aktarma-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="62395-128">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="62395-129">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="62395-129">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="62395-130">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="62395-130">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="62395-131">Yeni-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="62395-131">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="62395-132">Yeni-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="62395-132">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="62395-133">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="62395-133">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="62395-134">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="62395-134">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="62395-135">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="62395-135">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


