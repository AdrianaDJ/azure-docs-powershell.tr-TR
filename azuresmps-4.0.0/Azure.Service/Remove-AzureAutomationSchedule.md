---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2412F6BC-E338-4D9C-8982-C0668C1CA4C2
online version: ''
schema: 2.0.0
ms.openlocfilehash: b2b8ae09c79b420d7273fc6db23e23a6846a542e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106170"
---
# <span data-ttu-id="ad583-101">Remove-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ad583-101">Remove-AzureAutomationSchedule</span></span>

## <span data-ttu-id="ad583-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad583-102">SYNOPSIS</span></span>

<span data-ttu-id="ad583-103">Azure Otomasyonu zamanlamasını siler.</span><span class="sxs-lookup"><span data-stu-id="ad583-103">Deletes an Azure Automation schedule.</span></span>

## <span data-ttu-id="ad583-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ad583-104">SYNTAX</span></span>

```
Remove-AzureAutomationSchedule -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad583-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ad583-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="ad583-106">**Remove-Azureautomationzamanlama** cmdlet 'ı Microsoft Azure Otomasyonu 'ndan bir zamanlama siler.</span><span class="sxs-lookup"><span data-stu-id="ad583-106">The **Remove-AzureAutomationSchedule** cmdlet deletes a schedule from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="ad583-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ad583-107">EXAMPLES</span></span>

### <span data-ttu-id="ad583-108">Örnek 1: zamanlamayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="ad583-108">Example 1: Remove a schedule</span></span>
```
PS C:\> Remove-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "MySchedule"
```

<span data-ttu-id="ad583-109">Bu komut Myzamanlama adlı zamanlamayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ad583-109">This command removes the schedule named MySchedule.</span></span>

## <span data-ttu-id="ad583-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ad583-110">PARAMETERS</span></span>

### <span data-ttu-id="ad583-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ad583-111">-AutomationAccountName</span></span>
<span data-ttu-id="ad583-112">Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad583-112">Specifies the name of an Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad583-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ad583-113">-Force</span></span>
<span data-ttu-id="ad583-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="ad583-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad583-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="ad583-115">-Name</span></span>
<span data-ttu-id="ad583-116">Kaldırılacak zamanlamanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad583-116">Specifies the name of the schedule to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad583-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="ad583-117">-Profile</span></span>
<span data-ttu-id="ad583-118">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad583-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ad583-119">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="ad583-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad583-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="ad583-120">-Confirm</span></span>
<span data-ttu-id="ad583-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ad583-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad583-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad583-122">-WhatIf</span></span>
<span data-ttu-id="ad583-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ad583-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad583-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ad583-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad583-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad583-125">CommonParameters</span></span>
<span data-ttu-id="ad583-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ad583-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad583-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad583-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad583-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ad583-128">INPUTS</span></span>

## <span data-ttu-id="ad583-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ad583-129">OUTPUTS</span></span>

## <span data-ttu-id="ad583-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ad583-130">NOTES</span></span>

## <span data-ttu-id="ad583-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ad583-131">RELATED LINKS</span></span>

[<span data-ttu-id="ad583-132">Get-Azureautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="ad583-132">Get-AzureAutomationSchedule</span></span>](./Get-AzureAutomationSchedule.md)

[<span data-ttu-id="ad583-133">Yeni-Azureautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="ad583-133">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="ad583-134">Set-Azureautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="ad583-134">Set-AzureAutomationSchedule</span></span>](./Set-AzureAutomationSchedule.md)


