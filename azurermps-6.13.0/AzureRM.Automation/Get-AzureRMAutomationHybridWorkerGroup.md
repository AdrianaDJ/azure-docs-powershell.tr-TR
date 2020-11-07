---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9B0BBBB4-A7A0-4243-9264-362A00F5B399
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationHybridWorkerGroup.md
ms.openlocfilehash: 8fe4c554fd781d198af6bea784a433c141c2d41d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763919"
---
# <span data-ttu-id="74399-101">Get-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="74399-101">Get-AzureRmAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="74399-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74399-102">SYNOPSIS</span></span>
<span data-ttu-id="74399-103">Karma runbook çalışanı gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="74399-103">Gets hybrid runbook worker groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74399-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="74399-104">SYNTAX</span></span>

### <span data-ttu-id="74399-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="74399-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationHybridWorkerGroup [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74399-106">ByName</span><span class="sxs-lookup"><span data-stu-id="74399-106">ByName</span></span>
```
Get-AzureRmAutomationHybridWorkerGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74399-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="74399-107">DESCRIPTION</span></span>
<span data-ttu-id="74399-108">**Get-AzureRmAutomationHybridWorkerGroup** cmdlet 'ı Azure Otomasyonu karma runbook çalışanı gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="74399-108">The **Get-AzureRmAutomationHybridWorkerGroup** cmdlet gets Azure Automation hybrid runbook worker groups.</span></span>
<span data-ttu-id="74399-109">Belirli bir grubu almak için adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="74399-109">To get a specific group, specify its name.</span></span>

## <span data-ttu-id="74399-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="74399-110">EXAMPLES</span></span>

### <span data-ttu-id="74399-111">Örnek 1: tüm karma runbook çalışanı gruplarını al</span><span class="sxs-lookup"><span data-stu-id="74399-111">Example 1: Get all hybrid runbook worker groups</span></span>
```
PS C:\>Get-AzureRMAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="74399-112">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm karma runbook çalışanı gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="74399-112">This command gets all hybrid runbook worker groups in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="74399-113">Örnek 2: tek bir karma runbook çalışanı grubu edinin</span><span class="sxs-lookup"><span data-stu-id="74399-113">Example 2: Get a single hybrid runbook worker group</span></span>
```
PS C:\>Get-AzureRMAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17" -Name "HybridRunbookWorkerGroup01"
```

<span data-ttu-id="74399-114">Bu komut, Contoso17 adındaki Otomasyon hesabında HybridRunbookWorkerGroup01 adındaki karma runbook çalışanı grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="74399-114">This command gets the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="74399-115">Örnek 3: karma runbook çalışanı grubundaki çalışanları edinme</span><span class="sxs-lookup"><span data-stu-id="74399-115">Example 3: Get the workers in a hybrid runbook worker group</span></span>
```
PS C:\>(Get-AzureRMAutomationHybridWorker -ResourceGroupName ResourceGroupName01 -AutomationAccountName Contoso17 -Name "HybridRunbookWorkerGroup01" ).RunbookWorker
```

<span data-ttu-id="74399-116">Bu komut, karma runbook çalışanı grubundaki karma runbook çalışanlarına Contoso17 adındaki Otomasyon hesabında HybridRunbookWorkerGroup01 adındaki karma runbook çalışanlarını getirir.</span><span class="sxs-lookup"><span data-stu-id="74399-116">This command gets the hybrid runbook workers in the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="74399-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="74399-117">PARAMETERS</span></span>

### <span data-ttu-id="74399-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="74399-118">-AutomationAccountName</span></span>
<span data-ttu-id="74399-119">Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="74399-119">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="74399-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74399-120">-DefaultProfile</span></span>
<span data-ttu-id="74399-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="74399-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74399-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="74399-122">-Name</span></span>
<span data-ttu-id="74399-123">Karma Runbook Worker grup adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="74399-123">Specifies the hybrid runbook worker group name.</span></span>

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

### <span data-ttu-id="74399-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74399-124">-ResourceGroupName</span></span>
<span data-ttu-id="74399-125">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="74399-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="74399-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74399-126">CommonParameters</span></span>
<span data-ttu-id="74399-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="74399-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74399-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74399-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74399-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="74399-129">INPUTS</span></span>

### <span data-ttu-id="74399-130">System. String</span><span class="sxs-lookup"><span data-stu-id="74399-130">System.String</span></span>
<span data-ttu-id="74399-131">Parametreler: Name (ByValue)</span><span class="sxs-lookup"><span data-stu-id="74399-131">Parameters: Name (ByValue)</span></span>

## <span data-ttu-id="74399-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="74399-132">OUTPUTS</span></span>

### <span data-ttu-id="74399-133">Microsoft. Azure. Commands. Automation. model. HybridRunbookWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="74399-133">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span></span>

## <span data-ttu-id="74399-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="74399-134">NOTES</span></span>

## <span data-ttu-id="74399-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="74399-135">RELATED LINKS</span></span>
