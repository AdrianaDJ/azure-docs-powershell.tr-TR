---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationSchedule.md
ms.openlocfilehash: 78e34c5d3d94a964fbff6d0cbaa74c9dd3dd2177
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592813"
---
# <span data-ttu-id="3ae3d-101">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="3ae3d-101">Get-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="3ae3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ae3d-102">SYNOPSIS</span></span>
<span data-ttu-id="3ae3d-103">Otomasyon zamanlaması alır.</span><span class="sxs-lookup"><span data-stu-id="3ae3d-103">Gets an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ae3d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3ae3d-104">SYNTAX</span></span>

### <span data-ttu-id="3ae3d-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3ae3d-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ae3d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="3ae3d-106">ByName</span></span>
```
Get-AzureRmAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ae3d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3ae3d-107">DESCRIPTION</span></span>
<span data-ttu-id="3ae3d-108">**Get-Azurermautomationzamanlama** cmdlet 'ı bir Azure Otomasyonu zamanlaması alır.</span><span class="sxs-lookup"><span data-stu-id="3ae3d-108">The **Get-AzureRmAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="3ae3d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3ae3d-109">EXAMPLES</span></span>

### <span data-ttu-id="3ae3d-110">Örnek 1: zamanlama alma</span><span class="sxs-lookup"><span data-stu-id="3ae3d-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3ae3d-111">Bu komut, DailySchedule08 adlı zamanlamayı alır.</span><span class="sxs-lookup"><span data-stu-id="3ae3d-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="3ae3d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3ae3d-112">PARAMETERS</span></span>

### <span data-ttu-id="3ae3d-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3ae3d-113">-AutomationAccountName</span></span>
<span data-ttu-id="3ae3d-114">Bu cmdlet 'in zamanlama aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ae3d-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="3ae3d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ae3d-115">-DefaultProfile</span></span>
<span data-ttu-id="3ae3d-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3ae3d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ae3d-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="3ae3d-117">-Name</span></span>
<span data-ttu-id="3ae3d-118">Bu cmdlet 'in aldığı zamanlamanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ae3d-118">Specifies the name of a schedule that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3ae3d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ae3d-119">-ResourceGroupName</span></span>
<span data-ttu-id="3ae3d-120">Bu cmdlet 'in zamanlama aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ae3d-120">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="3ae3d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ae3d-121">CommonParameters</span></span>
<span data-ttu-id="3ae3d-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3ae3d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ae3d-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ae3d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ae3d-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3ae3d-124">INPUTS</span></span>

### <span data-ttu-id="3ae3d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="3ae3d-125">System.String</span></span>

## <span data-ttu-id="3ae3d-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3ae3d-126">OUTPUTS</span></span>

### <span data-ttu-id="3ae3d-127">Microsoft. Azure. Commands. Automation. model. zamanlama</span><span class="sxs-lookup"><span data-stu-id="3ae3d-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="3ae3d-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3ae3d-128">NOTES</span></span>

## <span data-ttu-id="3ae3d-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3ae3d-129">RELATED LINKS</span></span>

[<span data-ttu-id="3ae3d-130">Yeni-Azurermautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="3ae3d-130">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="3ae3d-131">Remove-Azurermautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="3ae3d-131">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)

[<span data-ttu-id="3ae3d-132">Set-Azurermautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="3ae3d-132">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


