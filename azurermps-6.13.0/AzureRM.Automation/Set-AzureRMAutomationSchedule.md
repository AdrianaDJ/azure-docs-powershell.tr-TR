---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6429C564-1995-4D9B-BF9B-963B4F5FB3BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationSchedule.md
ms.openlocfilehash: 76cc8117458db23f947a998d29de09a900bb6d42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762491"
---
# <span data-ttu-id="a355d-101">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="a355d-101">Set-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="a355d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a355d-102">SYNOPSIS</span></span>
<span data-ttu-id="a355d-103">Otomasyon zamanlamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a355d-103">Modifies an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a355d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a355d-104">SYNTAX</span></span>

```
Set-AzureRmAutomationSchedule [-Name] <String> [-IsEnabled <Boolean>] [-Description <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a355d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a355d-105">DESCRIPTION</span></span>
<span data-ttu-id="a355d-106">**Set-Azurermautomationzamanlama** cmdlet 'ı Azure Otomasyonu 'nda zamanlamayı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a355d-106">The **Set-AzureRmAutomationSchedule** cmdlet modifies a schedule in Azure Automation.</span></span>

## <span data-ttu-id="a355d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a355d-107">EXAMPLES</span></span>

### <span data-ttu-id="a355d-108">Örnek 1: zamanlamayı değiştirme</span><span class="sxs-lookup"><span data-stu-id="a355d-108">Example 1: Modify a schedule</span></span>
```
PS C:\>Set-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a355d-109">Bu komut, Schedule01 adlı zamanlamanın açıklamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a355d-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="a355d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a355d-110">PARAMETERS</span></span>

### <span data-ttu-id="a355d-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a355d-111">-AutomationAccountName</span></span>
<span data-ttu-id="a355d-112">Bu cmdlet 'in zamanlamayı değiştirdiği Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a355d-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="a355d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a355d-113">-DefaultProfile</span></span>
<span data-ttu-id="a355d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a355d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a355d-115">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="a355d-115">-Description</span></span>
<span data-ttu-id="a355d-116">Zamanlama için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="a355d-116">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="a355d-117">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="a355d-117">-IsEnabled</span></span>
<span data-ttu-id="a355d-118">Bu cmdlet 'in zamanlamayı etkinleştirilip etkinleştirilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a355d-118">Specifies whether this cmdlet enables the schedule.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a355d-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="a355d-119">-Name</span></span>
<span data-ttu-id="a355d-120">Bu cmdlet 'in değiştirdiği zamanlamanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a355d-120">Specifies the name for the schedule that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a355d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a355d-121">-ResourceGroupName</span></span>
<span data-ttu-id="a355d-122">Bu cmdlet 'in zamanlamayı değiştirdiği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a355d-122">Specifies the name of a resource group for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="a355d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a355d-123">CommonParameters</span></span>
<span data-ttu-id="a355d-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a355d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a355d-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a355d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a355d-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a355d-126">INPUTS</span></span>

### <span data-ttu-id="a355d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a355d-127">System.String</span></span>

### <span data-ttu-id="a355d-128">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a355d-128">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="a355d-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a355d-129">OUTPUTS</span></span>

### <span data-ttu-id="a355d-130">Microsoft. Azure. Commands. Automation. model. zamanlama</span><span class="sxs-lookup"><span data-stu-id="a355d-130">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="a355d-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a355d-131">NOTES</span></span>

## <span data-ttu-id="a355d-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a355d-132">RELATED LINKS</span></span>

[<span data-ttu-id="a355d-133">Get-Azurermautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="a355d-133">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="a355d-134">Yeni-Azurermautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="a355d-134">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="a355d-135">Remove-Azurermautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="a355d-135">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)


