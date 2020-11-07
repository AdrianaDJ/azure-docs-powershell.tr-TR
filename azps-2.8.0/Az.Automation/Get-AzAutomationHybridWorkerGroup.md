---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9B0BBBB4-A7A0-4243-9264-362A00F5B399
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: 7481975d880d3d43508756ac2daec3e665878ee0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753324"
---
# <span data-ttu-id="29bb7-101">Get-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="29bb7-101">Get-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="29bb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29bb7-102">SYNOPSIS</span></span>
<span data-ttu-id="29bb7-103">Karma runbook çalışanı gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="29bb7-103">Gets hybrid runbook worker groups.</span></span>

## <span data-ttu-id="29bb7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="29bb7-104">SYNTAX</span></span>

### <span data-ttu-id="29bb7-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="29bb7-105">ByAll (Default)</span></span>
```
Get-AzAutomationHybridWorkerGroup [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29bb7-106">ByName</span><span class="sxs-lookup"><span data-stu-id="29bb7-106">ByName</span></span>
```
Get-AzAutomationHybridWorkerGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29bb7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="29bb7-107">DESCRIPTION</span></span>
<span data-ttu-id="29bb7-108">**Get-AzAutomationHybridWorkerGroup** cmdlet 'ı Azure Otomasyonu karma runbook çalışanı gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="29bb7-108">The **Get-AzAutomationHybridWorkerGroup** cmdlet gets Azure Automation hybrid runbook worker groups.</span></span>
<span data-ttu-id="29bb7-109">Belirli bir grubu almak için adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="29bb7-109">To get a specific group, specify its name.</span></span>

## <span data-ttu-id="29bb7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="29bb7-110">EXAMPLES</span></span>

### <span data-ttu-id="29bb7-111">Örnek 1: tüm karma runbook çalışanı gruplarını al</span><span class="sxs-lookup"><span data-stu-id="29bb7-111">Example 1: Get all hybrid runbook worker groups</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="29bb7-112">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm karma runbook çalışanı gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="29bb7-112">This command gets all hybrid runbook worker groups in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="29bb7-113">Örnek 2: tek bir karma runbook çalışanı grubu edinin</span><span class="sxs-lookup"><span data-stu-id="29bb7-113">Example 2: Get a single hybrid runbook worker group</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17" -Name "HybridRunbookWorkerGroup01"
```

<span data-ttu-id="29bb7-114">Bu komut, Contoso17 adındaki Otomasyon hesabında HybridRunbookWorkerGroup01 adındaki karma runbook çalışanı grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="29bb7-114">This command gets the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="29bb7-115">Örnek 3: karma runbook çalışanı grubundaki çalışanları edinme</span><span class="sxs-lookup"><span data-stu-id="29bb7-115">Example 3: Get the workers in a hybrid runbook worker group</span></span>
```
PS C:\>(Get-AzAutomationHybridWorker -ResourceGroupName ResourceGroupName01 -AutomationAccountName Contoso17 -Name "HybridRunbookWorkerGroup01" ).RunbookWorker
```

<span data-ttu-id="29bb7-116">Bu komut, karma runbook çalışanı grubundaki karma runbook çalışanlarına Contoso17 adındaki Otomasyon hesabında HybridRunbookWorkerGroup01 adındaki karma runbook çalışanlarını getirir.</span><span class="sxs-lookup"><span data-stu-id="29bb7-116">This command gets the hybrid runbook workers in the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="29bb7-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="29bb7-117">PARAMETERS</span></span>

### <span data-ttu-id="29bb7-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="29bb7-118">-AutomationAccountName</span></span>
<span data-ttu-id="29bb7-119">Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="29bb7-119">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="29bb7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29bb7-120">-DefaultProfile</span></span>
<span data-ttu-id="29bb7-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="29bb7-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29bb7-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="29bb7-122">-Name</span></span>
<span data-ttu-id="29bb7-123">Karma Runbook Worker grup adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="29bb7-123">Specifies the hybrid runbook worker group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Group

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29bb7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29bb7-124">-ResourceGroupName</span></span>
<span data-ttu-id="29bb7-125">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="29bb7-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="29bb7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29bb7-126">CommonParameters</span></span>
<span data-ttu-id="29bb7-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="29bb7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29bb7-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29bb7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29bb7-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="29bb7-129">INPUTS</span></span>

### <span data-ttu-id="29bb7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="29bb7-130">System.String</span></span>

## <span data-ttu-id="29bb7-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="29bb7-131">OUTPUTS</span></span>

### <span data-ttu-id="29bb7-132">Microsoft. Azure. Commands. Automation. model. HybridRunbookWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="29bb7-132">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span></span>

## <span data-ttu-id="29bb7-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="29bb7-133">NOTES</span></span>

## <span data-ttu-id="29bb7-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="29bb7-134">RELATED LINKS</span></span>
