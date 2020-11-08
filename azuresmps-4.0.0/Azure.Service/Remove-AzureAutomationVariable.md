---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2D89557B-4B8B-43EE-8453-D55FCE0C2CE0
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8fdd9dd886e4056f2cb7e547098e5d3ab75a547
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106169"
---
# <span data-ttu-id="e6fb5-101">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e6fb5-101">Remove-AzureAutomationVariable</span></span>

## <span data-ttu-id="e6fb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6fb5-102">SYNOPSIS</span></span>

<span data-ttu-id="e6fb5-103">Otomasyon değişkenini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e6fb5-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="e6fb5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e6fb5-104">SYNTAX</span></span>

```
Remove-AzureAutomationVariable -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e6fb5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e6fb5-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="e6fb5-106">**Remove-AzureAutomationVariable** cmdlet 'ı, Microsoft Azure Otomasyonu 'ndan bir değişkeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e6fb5-106">The **Remove-AzureAutomationVariable** cmdlet removes a variable from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="e6fb5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e6fb5-107">EXAMPLES</span></span>

### <span data-ttu-id="e6fb5-108">Örnek 1: bir değişkeni kaldırma</span><span class="sxs-lookup"><span data-stu-id="e6fb5-108">Example 1: Remove a variable</span></span>
```
PS C:\> Remove-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyStringVariable" -Force
```

<span data-ttu-id="e6fb5-109">Bu komut, kullanıcı doğrulaması istemeden Contoso17 adlı Otomasyon hesabındaki MyStringVariable adlı bir değişkeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e6fb5-109">This command removes a variable named MyStringVariable in the Automation account named Contoso17 without prompting for user validation.</span></span>

## <span data-ttu-id="e6fb5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e6fb5-110">PARAMETERS</span></span>

### <span data-ttu-id="e6fb5-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e6fb5-111">-AutomationAccountName</span></span>
<span data-ttu-id="e6fb5-112">Değişkenin olduğu Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6fb5-112">Specifies the name of the Automation account with the variable.</span></span>

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

### <span data-ttu-id="e6fb5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e6fb5-113">-Force</span></span>
<span data-ttu-id="e6fb5-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="e6fb5-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e6fb5-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="e6fb5-115">-Name</span></span>
<span data-ttu-id="e6fb5-116">Değişkenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6fb5-116">Specifies the name of the variable.</span></span>

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

### <span data-ttu-id="e6fb5-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="e6fb5-117">-Profile</span></span>
<span data-ttu-id="e6fb5-118">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6fb5-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e6fb5-119">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="e6fb5-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e6fb5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6fb5-120">CommonParameters</span></span>
<span data-ttu-id="e6fb5-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e6fb5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6fb5-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6fb5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6fb5-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e6fb5-123">INPUTS</span></span>

## <span data-ttu-id="e6fb5-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e6fb5-124">OUTPUTS</span></span>

## <span data-ttu-id="e6fb5-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e6fb5-125">NOTES</span></span>

## <span data-ttu-id="e6fb5-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e6fb5-126">RELATED LINKS</span></span>

[<span data-ttu-id="e6fb5-127">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e6fb5-127">Get-AzureAutomationVariable</span></span>](./Get-AzureAutomationVariable.md)

[<span data-ttu-id="e6fb5-128">New-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e6fb5-128">New-AzureAutomationVariable</span></span>](./New-AzureAutomationVariable.md)

[<span data-ttu-id="e6fb5-129">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e6fb5-129">Set-AzureAutomationVariable</span></span>](./Set-AzureAutomationVariable.md)


