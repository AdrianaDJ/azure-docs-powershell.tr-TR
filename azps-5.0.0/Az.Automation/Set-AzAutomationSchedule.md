---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6429C564-1995-4D9B-BF9B-963B4F5FB3BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationSchedule.md
ms.openlocfilehash: 3de9658011bd781d98e16c1ba996a6951c548975
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277659"
---
# <span data-ttu-id="5ba53-101">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="5ba53-101">Set-AzAutomationSchedule</span></span>

## <span data-ttu-id="5ba53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ba53-102">SYNOPSIS</span></span>
<span data-ttu-id="5ba53-103">Otomasyon zamanlamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5ba53-103">Modifies an Automation schedule.</span></span>

## <span data-ttu-id="5ba53-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5ba53-104">SYNTAX</span></span>

```
Set-AzAutomationSchedule [-Name] <String> [-IsEnabled <Boolean>] [-Description <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ba53-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5ba53-105">DESCRIPTION</span></span>
<span data-ttu-id="5ba53-106">**Set-Azautomationzamanlama** cmdlet 'ı, Azure Otomasyonu 'nda bir zamanlamayı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5ba53-106">The **Set-AzAutomationSchedule** cmdlet modifies a schedule in Azure Automation.</span></span>

## <span data-ttu-id="5ba53-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5ba53-107">EXAMPLES</span></span>

### <span data-ttu-id="5ba53-108">Örnek 1: zamanlamayı değiştirme</span><span class="sxs-lookup"><span data-stu-id="5ba53-108">Example 1: Modify a schedule</span></span>
```
PS C:\>Set-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5ba53-109">Bu komut, Schedule01 adlı zamanlamanın açıklamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5ba53-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="5ba53-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5ba53-110">PARAMETERS</span></span>

### <span data-ttu-id="5ba53-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5ba53-111">-AutomationAccountName</span></span>
<span data-ttu-id="5ba53-112">Bu cmdlet 'in zamanlamayı değiştirdiği Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ba53-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="5ba53-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ba53-113">-DefaultProfile</span></span>
<span data-ttu-id="5ba53-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5ba53-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ba53-115">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="5ba53-115">-Description</span></span>
<span data-ttu-id="5ba53-116">Zamanlama için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ba53-116">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="5ba53-117">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="5ba53-117">-IsEnabled</span></span>
<span data-ttu-id="5ba53-118">Bu cmdlet 'in zamanlamayı etkinleştirilip etkinleştirilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ba53-118">Specifies whether this cmdlet enables the schedule.</span></span>

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

### <span data-ttu-id="5ba53-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="5ba53-119">-Name</span></span>
<span data-ttu-id="5ba53-120">Bu cmdlet 'in değiştirdiği zamanlamanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ba53-120">Specifies the name for the schedule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5ba53-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ba53-121">-ResourceGroupName</span></span>
<span data-ttu-id="5ba53-122">Bu cmdlet 'in zamanlamayı değiştirdiği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ba53-122">Specifies the name of a resource group for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="5ba53-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ba53-123">CommonParameters</span></span>
<span data-ttu-id="5ba53-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5ba53-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ba53-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ba53-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ba53-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5ba53-126">INPUTS</span></span>

### <span data-ttu-id="5ba53-127">System. String</span><span class="sxs-lookup"><span data-stu-id="5ba53-127">System.String</span></span>

### <span data-ttu-id="5ba53-128">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="5ba53-128">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5ba53-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5ba53-129">OUTPUTS</span></span>

### <span data-ttu-id="5ba53-130">Microsoft. Azure. Commands. Automation. model. zamanlama</span><span class="sxs-lookup"><span data-stu-id="5ba53-130">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="5ba53-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5ba53-131">NOTES</span></span>

## <span data-ttu-id="5ba53-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5ba53-132">RELATED LINKS</span></span>

[<span data-ttu-id="5ba53-133">Get-Azautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="5ba53-133">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="5ba53-134">Yeni-Azautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="5ba53-134">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="5ba53-135">Remove-Azautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="5ba53-135">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)


