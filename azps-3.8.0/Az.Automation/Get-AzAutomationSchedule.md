---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
ms.openlocfilehash: a07208db434a43730b75542bb0f8959ae68423d1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098146"
---
# <span data-ttu-id="3f8dd-101">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="3f8dd-101">Get-AzAutomationSchedule</span></span>

## <span data-ttu-id="3f8dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f8dd-102">SYNOPSIS</span></span>
<span data-ttu-id="3f8dd-103">Otomasyon zamanlaması alır.</span><span class="sxs-lookup"><span data-stu-id="3f8dd-103">Gets an Automation schedule.</span></span>

## <span data-ttu-id="3f8dd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3f8dd-104">SYNTAX</span></span>

### <span data-ttu-id="3f8dd-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3f8dd-105">ByAll (Default)</span></span>
```
Get-AzAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f8dd-106">ByName</span><span class="sxs-lookup"><span data-stu-id="3f8dd-106">ByName</span></span>
```
Get-AzAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f8dd-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3f8dd-107">DESCRIPTION</span></span>
<span data-ttu-id="3f8dd-108">**Get-Azautomationzamanlama** cmdlet 'ı bir Azure Otomasyonu zamanlaması alır.</span><span class="sxs-lookup"><span data-stu-id="3f8dd-108">The **Get-AzAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="3f8dd-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3f8dd-109">EXAMPLES</span></span>

### <span data-ttu-id="3f8dd-110">Örnek 1: zamanlama alma</span><span class="sxs-lookup"><span data-stu-id="3f8dd-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3f8dd-111">Bu komut, DailySchedule08 adlı zamanlamayı alır.</span><span class="sxs-lookup"><span data-stu-id="3f8dd-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="3f8dd-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3f8dd-112">PARAMETERS</span></span>

### <span data-ttu-id="3f8dd-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3f8dd-113">-AutomationAccountName</span></span>
<span data-ttu-id="3f8dd-114">Bu cmdlet 'in zamanlama aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f8dd-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="3f8dd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f8dd-115">-DefaultProfile</span></span>
<span data-ttu-id="3f8dd-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3f8dd-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f8dd-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="3f8dd-117">-Name</span></span>
<span data-ttu-id="3f8dd-118">Bu cmdlet 'in aldığı zamanlamanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f8dd-118">Specifies the name of a schedule that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f8dd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f8dd-119">-ResourceGroupName</span></span>
<span data-ttu-id="3f8dd-120">Bu cmdlet 'in zamanlama aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f8dd-120">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="3f8dd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f8dd-121">CommonParameters</span></span>
<span data-ttu-id="3f8dd-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3f8dd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f8dd-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f8dd-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f8dd-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3f8dd-124">INPUTS</span></span>

### <span data-ttu-id="3f8dd-125">System. String</span><span class="sxs-lookup"><span data-stu-id="3f8dd-125">System.String</span></span>

## <span data-ttu-id="3f8dd-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3f8dd-126">OUTPUTS</span></span>

### <span data-ttu-id="3f8dd-127">Microsoft. Azure. Commands. Automation. model. zamanlama</span><span class="sxs-lookup"><span data-stu-id="3f8dd-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="3f8dd-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3f8dd-128">NOTES</span></span>

## <span data-ttu-id="3f8dd-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3f8dd-129">RELATED LINKS</span></span>

[<span data-ttu-id="3f8dd-130">Yeni-Azautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="3f8dd-130">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="3f8dd-131">Remove-Azautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="3f8dd-131">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="3f8dd-132">Set-Azautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="3f8dd-132">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)

