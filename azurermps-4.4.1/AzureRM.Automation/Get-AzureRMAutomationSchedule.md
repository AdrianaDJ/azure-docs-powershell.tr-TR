---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationSchedule.md
ms.openlocfilehash: 1252864be8e55638ec5e982bd075aec647b68a18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595040"
---
# <span data-ttu-id="d3f05-101">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="d3f05-101">Get-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="d3f05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3f05-102">SYNOPSIS</span></span>
<span data-ttu-id="d3f05-103">Otomasyon zamanlaması alır.</span><span class="sxs-lookup"><span data-stu-id="d3f05-103">Gets an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3f05-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d3f05-104">SYNTAX</span></span>

### <span data-ttu-id="d3f05-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d3f05-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3f05-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d3f05-106">ByName</span></span>
```
Get-AzureRmAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3f05-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d3f05-107">DESCRIPTION</span></span>
<span data-ttu-id="d3f05-108">**Get-Azurermautomationzamanlama** cmdlet 'ı bir Azure Otomasyonu zamanlaması alır.</span><span class="sxs-lookup"><span data-stu-id="d3f05-108">The **Get-AzureRmAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="d3f05-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d3f05-109">EXAMPLES</span></span>

### <span data-ttu-id="d3f05-110">Örnek 1: zamanlama alma</span><span class="sxs-lookup"><span data-stu-id="d3f05-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d3f05-111">Bu komut, DailySchedule08 adlı zamanlamayı alır.</span><span class="sxs-lookup"><span data-stu-id="d3f05-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="d3f05-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d3f05-112">PARAMETERS</span></span>

### <span data-ttu-id="d3f05-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d3f05-113">-AutomationAccountName</span></span>
<span data-ttu-id="d3f05-114">Bu cmdlet 'in zamanlama aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3f05-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="d3f05-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="d3f05-115">-Name</span></span>
<span data-ttu-id="d3f05-116">Bu cmdlet 'in aldığı zamanlamanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3f05-116">Specifies the name of a schedule that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d3f05-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3f05-117">-ResourceGroupName</span></span>
<span data-ttu-id="d3f05-118">Bu cmdlet 'in zamanlama aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3f05-118">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="d3f05-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3f05-119">-DefaultProfile</span></span>
<span data-ttu-id="d3f05-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d3f05-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3f05-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3f05-121">CommonParameters</span></span>
<span data-ttu-id="d3f05-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d3f05-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3f05-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3f05-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3f05-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d3f05-124">INPUTS</span></span>

## <span data-ttu-id="d3f05-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d3f05-125">OUTPUTS</span></span>

### <span data-ttu-id="d3f05-126">Microsoft. Azure. Commands. Automation. model. zamanlama</span><span class="sxs-lookup"><span data-stu-id="d3f05-126">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="d3f05-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d3f05-127">NOTES</span></span>

## <span data-ttu-id="d3f05-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d3f05-128">RELATED LINKS</span></span>

[<span data-ttu-id="d3f05-129">Yeni-Azurermautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="d3f05-129">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="d3f05-130">Remove-Azurermautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="d3f05-130">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)

[<span data-ttu-id="d3f05-131">Set-Azurermautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="d3f05-131">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


