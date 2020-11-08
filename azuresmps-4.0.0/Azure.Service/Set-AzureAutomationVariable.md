---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 47664B13-5D63-4012-80E1-7982C8FE22E1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20edd29629cb5dbbfa6f3f538d1530e9c0692e6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106068"
---
# <span data-ttu-id="c6897-101">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="c6897-101">Set-AzureAutomationVariable</span></span>

## <span data-ttu-id="c6897-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6897-102">SYNOPSIS</span></span>

<span data-ttu-id="c6897-103">Otomasyon değişkenini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c6897-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="c6897-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c6897-104">SYNTAX</span></span>

### <span data-ttu-id="c6897-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="c6897-105">UpdateVariableValue</span></span>
```
Set-AzureAutomationVariable -Name <String> -Encrypted <Boolean> -Value <Object> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c6897-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="c6897-106">UpdateVariableDescription</span></span>
```
Set-AzureAutomationVariable -Name <String> -Description <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c6897-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c6897-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="c6897-108">**Set-AzureAutomationVariable** cmdlet 'ı, Microsoft Azure Otomasyonu 'nda bir değişkenin değerini veya açıklamasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c6897-108">The **Set-AzureAutomationVariable** cmdlet modifies the value or description of a variable in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="c6897-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c6897-109">EXAMPLES</span></span>

### <span data-ttu-id="c6897-110">Örnek 1: değişkenin değerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="c6897-110">Example 1: Set the value of a variable</span></span>
```
PS C:\> Set-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyStringVariable" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="c6897-111">Bu komut, Contoso17 adlı Azure Otomasyonu hesabındaki MyStringVariable adlı değişken için yeni bir değer ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c6897-111">This command sets a new value for the variable named MyStringVariable in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="c6897-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c6897-112">PARAMETERS</span></span>

### <span data-ttu-id="c6897-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c6897-113">-AutomationAccountName</span></span>
<span data-ttu-id="c6897-114">Değişkenin olduğu Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6897-114">Specifies the name of the Automation account with the variable.</span></span>

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

### <span data-ttu-id="c6897-115">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="c6897-115">-Description</span></span>
<span data-ttu-id="c6897-116">Değişken için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6897-116">Specifies a description for the variable.</span></span>

```yaml
Type: String
Parameter Sets: UpdateVariableDescription
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6897-117">-Şifreli</span><span class="sxs-lookup"><span data-stu-id="c6897-117">-Encrypted</span></span>
<span data-ttu-id="c6897-118">Değişkenin şifrelenip şifrelenmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6897-118">Indicates whether to encrypt the variable.</span></span>

```yaml
Type: Boolean
Parameter Sets: UpdateVariableValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6897-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="c6897-119">-Name</span></span>
<span data-ttu-id="c6897-120">Değişkenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6897-120">Specifies the name of the variable.</span></span>

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

### <span data-ttu-id="c6897-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="c6897-121">-Profile</span></span>
<span data-ttu-id="c6897-122">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6897-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c6897-123">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="c6897-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c6897-124">-Değer</span><span class="sxs-lookup"><span data-stu-id="c6897-124">-Value</span></span>
<span data-ttu-id="c6897-125">Değişken için bir değer belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6897-125">Specifies a value for the variable.</span></span>

```yaml
Type: Object
Parameter Sets: UpdateVariableValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6897-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6897-126">CommonParameters</span></span>
<span data-ttu-id="c6897-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c6897-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6897-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6897-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6897-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c6897-129">INPUTS</span></span>

## <span data-ttu-id="c6897-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c6897-130">OUTPUTS</span></span>

### <span data-ttu-id="c6897-131">Microsoft. Azure. Commands. Automation. model. Variable</span><span class="sxs-lookup"><span data-stu-id="c6897-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="c6897-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c6897-132">NOTES</span></span>

## <span data-ttu-id="c6897-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c6897-133">RELATED LINKS</span></span>

[<span data-ttu-id="c6897-134">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="c6897-134">Get-AzureAutomationVariable</span></span>](./Get-AzureAutomationVariable.md)

[<span data-ttu-id="c6897-135">New-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="c6897-135">New-AzureAutomationVariable</span></span>](./New-AzureAutomationVariable.md)

[<span data-ttu-id="c6897-136">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="c6897-136">Remove-AzureAutomationVariable</span></span>](./Remove-AzureAutomationVariable.md)


