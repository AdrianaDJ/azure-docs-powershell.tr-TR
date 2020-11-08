---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: CC6AF515-2F43-4E1B-BCBB-8DA23F3C6CBD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8687cc00e9ba83c427666e08d0ad46c9aab45e02
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105653"
---
# <span data-ttu-id="1886b-101">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="1886b-101">Get-AzureAutomationVariable</span></span>

## <span data-ttu-id="1886b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1886b-102">SYNOPSIS</span></span>

<span data-ttu-id="1886b-103">Bir Otomasyon değişkeni alır.</span><span class="sxs-lookup"><span data-stu-id="1886b-103">Gets an Automation variable.</span></span>

## <span data-ttu-id="1886b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1886b-104">SYNTAX</span></span>

### <span data-ttu-id="1886b-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1886b-105">ByAll (Default)</span></span>
```
Get-AzureAutomationVariable -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1886b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="1886b-106">ByName</span></span>
```
Get-AzureAutomationVariable -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="1886b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1886b-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="1886b-108">**Get-AzureAutomationVariable** cmdlet 'i bir veya daha fazla Microsoft Azure Otomasyonu değişkenini alır.</span><span class="sxs-lookup"><span data-stu-id="1886b-108">The **Get-AzureAutomationVariable** cmdlet gets one or more Microsoft Azure Automation variables.</span></span>
<span data-ttu-id="1886b-109">Varsayılan olarak, tüm değişkenler döndürülür.</span><span class="sxs-lookup"><span data-stu-id="1886b-109">By default, all variables are returned.</span></span>
<span data-ttu-id="1886b-110">Belirli bir değişken almak için adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="1886b-110">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="1886b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1886b-111">EXAMPLES</span></span>

### <span data-ttu-id="1886b-112">Örnek 1: değişken alma</span><span class="sxs-lookup"><span data-stu-id="1886b-112">Example 1: Get a variable</span></span>
```
PS C:\> $variable = Get-AzureAutomationVariable -AutomationAccountName
PS C:\> "Contoso17" -Name "MyVariable"
PS C:\> $value = $variable.value
```

<span data-ttu-id="1886b-113">Bu komutlar MyVariable adlı bir Automation değişkeni alır ve değerini $value adlı bir değişkene atar.</span><span class="sxs-lookup"><span data-stu-id="1886b-113">These commands get an Automation variable called MyVariable and assign its value to a variable called $value.</span></span>

## <span data-ttu-id="1886b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1886b-114">PARAMETERS</span></span>

### <span data-ttu-id="1886b-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1886b-115">-AutomationAccountName</span></span>
<span data-ttu-id="1886b-116">Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1886b-116">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="1886b-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="1886b-117">-Name</span></span>
<span data-ttu-id="1886b-118">Bir değişkenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1886b-118">Specifies the name of a variable.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1886b-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="1886b-119">-Profile</span></span>
<span data-ttu-id="1886b-120">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1886b-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1886b-121">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="1886b-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1886b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1886b-122">CommonParameters</span></span>
<span data-ttu-id="1886b-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1886b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1886b-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1886b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1886b-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1886b-125">INPUTS</span></span>

## <span data-ttu-id="1886b-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1886b-126">OUTPUTS</span></span>

### <span data-ttu-id="1886b-127">Microsoft. Azure. Commands. Automation. model. Variable</span><span class="sxs-lookup"><span data-stu-id="1886b-127">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="1886b-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1886b-128">NOTES</span></span>

## <span data-ttu-id="1886b-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1886b-129">RELATED LINKS</span></span>

[<span data-ttu-id="1886b-130">New-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="1886b-130">New-AzureAutomationVariable</span></span>](./New-AzureAutomationVariable.md)

[<span data-ttu-id="1886b-131">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="1886b-131">Remove-AzureAutomationVariable</span></span>](./Remove-AzureAutomationVariable.md)

[<span data-ttu-id="1886b-132">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="1886b-132">Set-AzureAutomationVariable</span></span>](./Set-AzureAutomationVariable.md)


