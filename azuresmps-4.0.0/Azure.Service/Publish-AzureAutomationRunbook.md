---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 454948A7-CE50-4C5A-AEBF-789B1A94F27E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 62507f18e21c1e528f93f5de512e8ffc1fa2dfa3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105885"
---
# <span data-ttu-id="7dd85-101">Publish-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7dd85-101">Publish-AzureAutomationRunbook</span></span>

## <span data-ttu-id="7dd85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7dd85-102">SYNOPSIS</span></span>

<span data-ttu-id="7dd85-103">Runbook yayımlar.</span><span class="sxs-lookup"><span data-stu-id="7dd85-103">Publishes a runbook.</span></span>

## <span data-ttu-id="7dd85-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7dd85-104">SYNTAX</span></span>

```
Publish-AzureAutomationRunbook -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="7dd85-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7dd85-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="7dd85-106">**Publish-AzureAutomationRunbook** cmdlet 'ı, Microsoft Azure Otomasyonu 'nun üretim ortamında kullanılmak üzere bir runbook yayımlar.</span><span class="sxs-lookup"><span data-stu-id="7dd85-106">The **Publish-AzureAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Microsoft Azure Automation.</span></span>

## <span data-ttu-id="7dd85-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7dd85-107">EXAMPLES</span></span>

### <span data-ttu-id="7dd85-108">Örnek 1: runbook yayımlama</span><span class="sxs-lookup"><span data-stu-id="7dd85-108">Example 1: Publish a runbook</span></span>
```
PS C:\> Publish-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01"
```

<span data-ttu-id="7dd85-109">Bu komut, Contoso17 adındaki Otomasyon hesabında Runbk01 adındaki runbook 'u yayımlar.</span><span class="sxs-lookup"><span data-stu-id="7dd85-109">This command publishes the runbook named Runbk01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="7dd85-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7dd85-110">PARAMETERS</span></span>

### <span data-ttu-id="7dd85-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7dd85-111">-AutomationAccountName</span></span>
<span data-ttu-id="7dd85-112">Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7dd85-112">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="7dd85-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="7dd85-113">-Name</span></span>
<span data-ttu-id="7dd85-114">Runbook 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7dd85-114">Specifies the name of the runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dd85-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="7dd85-115">-Profile</span></span>
<span data-ttu-id="7dd85-116">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7dd85-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7dd85-117">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="7dd85-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7dd85-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dd85-118">CommonParameters</span></span>
<span data-ttu-id="7dd85-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7dd85-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dd85-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dd85-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dd85-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7dd85-121">INPUTS</span></span>

## <span data-ttu-id="7dd85-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7dd85-122">OUTPUTS</span></span>

## <span data-ttu-id="7dd85-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7dd85-123">NOTES</span></span>

## <span data-ttu-id="7dd85-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7dd85-124">RELATED LINKS</span></span>

[<span data-ttu-id="7dd85-125">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7dd85-125">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="7dd85-126">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7dd85-126">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="7dd85-127">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7dd85-127">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="7dd85-128">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7dd85-128">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="7dd85-129">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7dd85-129">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


