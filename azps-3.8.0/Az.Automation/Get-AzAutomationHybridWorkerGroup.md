---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9B0BBBB4-A7A0-4243-9264-362A00F5B399
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: d675c6e5b83f76451808f397427011ac3406e37a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098158"
---
# <span data-ttu-id="c689e-101">Get-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="c689e-101">Get-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="c689e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c689e-102">SYNOPSIS</span></span>
<span data-ttu-id="c689e-103">Karma runbook çalışanı gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="c689e-103">Gets hybrid runbook worker groups.</span></span>

## <span data-ttu-id="c689e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c689e-104">SYNTAX</span></span>

### <span data-ttu-id="c689e-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c689e-105">ByAll (Default)</span></span>
```
Get-AzAutomationHybridWorkerGroup [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c689e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c689e-106">ByName</span></span>
```
Get-AzAutomationHybridWorkerGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c689e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c689e-107">DESCRIPTION</span></span>
<span data-ttu-id="c689e-108">**Get-AzAutomationHybridWorkerGroup** cmdlet 'ı Azure Otomasyonu karma runbook çalışanı gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="c689e-108">The **Get-AzAutomationHybridWorkerGroup** cmdlet gets Azure Automation hybrid runbook worker groups.</span></span>
<span data-ttu-id="c689e-109">Belirli bir grubu almak için adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="c689e-109">To get a specific group, specify its name.</span></span>

## <span data-ttu-id="c689e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c689e-110">EXAMPLES</span></span>

### <span data-ttu-id="c689e-111">Örnek 1: tüm karma runbook çalışanı gruplarını al</span><span class="sxs-lookup"><span data-stu-id="c689e-111">Example 1: Get all hybrid runbook worker groups</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="c689e-112">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm karma runbook çalışanı gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="c689e-112">This command gets all hybrid runbook worker groups in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="c689e-113">Örnek 2: tek bir karma runbook çalışanı grubu edinin</span><span class="sxs-lookup"><span data-stu-id="c689e-113">Example 2: Get a single hybrid runbook worker group</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17" -Name "HybridRunbookWorkerGroup01"
```

<span data-ttu-id="c689e-114">Bu komut, Contoso17 adındaki Otomasyon hesabında HybridRunbookWorkerGroup01 adındaki karma runbook çalışanı grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="c689e-114">This command gets the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="c689e-115">Örnek 3: karma runbook çalışanı grubundaki çalışanları edinme</span><span class="sxs-lookup"><span data-stu-id="c689e-115">Example 3: Get the workers in a hybrid runbook worker group</span></span>
```
PS C:\>(Get-AzAutomationHybridWorker -ResourceGroupName ResourceGroupName01 -AutomationAccountName Contoso17 -Name "HybridRunbookWorkerGroup01" ).RunbookWorker
```

<span data-ttu-id="c689e-116">Bu komut, karma runbook çalışanı grubundaki karma runbook çalışanlarına Contoso17 adındaki Otomasyon hesabında HybridRunbookWorkerGroup01 adındaki karma runbook çalışanlarını getirir.</span><span class="sxs-lookup"><span data-stu-id="c689e-116">This command gets the hybrid runbook workers in the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="c689e-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c689e-117">PARAMETERS</span></span>

### <span data-ttu-id="c689e-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c689e-118">-AutomationAccountName</span></span>
<span data-ttu-id="c689e-119">Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c689e-119">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="c689e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c689e-120">-DefaultProfile</span></span>
<span data-ttu-id="c689e-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c689e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c689e-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="c689e-122">-Name</span></span>
<span data-ttu-id="c689e-123">Karma Runbook Worker grup adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c689e-123">Specifies the hybrid runbook worker group name.</span></span>

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

### <span data-ttu-id="c689e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c689e-124">-ResourceGroupName</span></span>
<span data-ttu-id="c689e-125">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c689e-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c689e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c689e-126">CommonParameters</span></span>
<span data-ttu-id="c689e-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c689e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c689e-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c689e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c689e-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c689e-129">INPUTS</span></span>

### <span data-ttu-id="c689e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c689e-130">System.String</span></span>

## <span data-ttu-id="c689e-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c689e-131">OUTPUTS</span></span>

### <span data-ttu-id="c689e-132">Microsoft. Azure. Commands. Automation. model. HybridRunbookWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="c689e-132">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span></span>

## <span data-ttu-id="c689e-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c689e-133">NOTES</span></span>

## <span data-ttu-id="c689e-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c689e-134">RELATED LINKS</span></span>
