---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: D88C6B17-5D0E-4E23-9C5C-DB38DED9061C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1518c351a67c84e6dacafd1fa8a394051f3bfeac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105931"
---
# <span data-ttu-id="e2c69-101">New-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e2c69-101">New-AzureAutomationVariable</span></span>

## <span data-ttu-id="e2c69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2c69-102">SYNOPSIS</span></span>

<span data-ttu-id="e2c69-103">Otomasyon değişkeni oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e2c69-103">Creates an Automation variable.</span></span>

## <span data-ttu-id="e2c69-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e2c69-104">SYNTAX</span></span>

```
New-AzureAutomationVariable -Name <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e2c69-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2c69-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="e2c69-106">**New-AzureAutomationVariable** cmdlet 'ı Microsoft Azure Otomasyonu 'nda bir değişken oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e2c69-106">The **New-AzureAutomationVariable** cmdlet creates a variable in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="e2c69-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e2c69-107">EXAMPLES</span></span>

### <span data-ttu-id="e2c69-108">Örnek 1: basit bir değer içeren yeni bir değişken oluşturma</span><span class="sxs-lookup"><span data-stu-id="e2c69-108">Example 1: Create a new variable with a simple value</span></span>
```
PS C:\> New-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyStringVariable" -Encrypted $False -Value "My String"
```

<span data-ttu-id="e2c69-109">Bu komut, Contoso17 adlı Azure Otomasyonu hesabında dize değeriyle MyStringVariable adlı yeni bir değişken oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e2c69-109">This command creates a new variable named MyStringVariable with a string value in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="e2c69-110">Örnek 2: karmaşık bir değer içeren yeni bir değişken oluşturma</span><span class="sxs-lookup"><span data-stu-id="e2c69-110">Example 2: Create a new variable with a complex value</span></span>
```
PS C:\> $vm = Get-AzureVM -ServiceName "MyVM" -Name "MyVM"
PS C:\> New-AzureAutomationVariable -AutomationAccountName "Contoso17" -Name "MyComplexVariable" -Encrypted $False -Value $vm
```

<span data-ttu-id="e2c69-111">Bu komutlar, Contoso17 adlı Otomasyon hesabında MyComplexVariable adlı yeni bir değişken oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e2c69-111">These commands create a new variable called MyComplexVariable in the Automation account named Contoso17.</span></span>
<span data-ttu-id="e2c69-112">Bu durumda bir sanal makine nesnesi olan değeri için karmaşık bir nesne kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e2c69-112">A complex object is used for its value, in this case a virtual machine object.</span></span>

## <span data-ttu-id="e2c69-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e2c69-113">PARAMETERS</span></span>

### <span data-ttu-id="e2c69-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e2c69-114">-AutomationAccountName</span></span>
<span data-ttu-id="e2c69-115">Değişkenin saklanacağı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2c69-115">Specifies the name of the Automation account the variable will be stored in.</span></span>

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

### <span data-ttu-id="e2c69-116">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="e2c69-116">-Description</span></span>
<span data-ttu-id="e2c69-117">Değişken için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2c69-117">Specifies a description for the variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2c69-118">-Şifreli</span><span class="sxs-lookup"><span data-stu-id="e2c69-118">-Encrypted</span></span>
<span data-ttu-id="e2c69-119">Değişken değerinin şifrelenmiş olarak depolanması gerekip gerekmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e2c69-119">Indicates whether the value of the variable should be stored encrypted.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2c69-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="e2c69-120">-Name</span></span>
<span data-ttu-id="e2c69-121">Değişken için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2c69-121">Specifies a name for the variable.</span></span>

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

### <span data-ttu-id="e2c69-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="e2c69-122">-Profile</span></span>
<span data-ttu-id="e2c69-123">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2c69-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e2c69-124">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="e2c69-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e2c69-125">-Değer</span><span class="sxs-lookup"><span data-stu-id="e2c69-125">-Value</span></span>
<span data-ttu-id="e2c69-126">Değişkende depolanacağı bir değer belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2c69-126">Specifies a value to store in the variable.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2c69-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2c69-127">CommonParameters</span></span>
<span data-ttu-id="e2c69-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e2c69-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2c69-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2c69-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2c69-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e2c69-130">INPUTS</span></span>

## <span data-ttu-id="e2c69-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e2c69-131">OUTPUTS</span></span>

### <span data-ttu-id="e2c69-132">Microsoft. Azure. Commands. Automation. model. Variable</span><span class="sxs-lookup"><span data-stu-id="e2c69-132">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="e2c69-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e2c69-133">NOTES</span></span>

## <span data-ttu-id="e2c69-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e2c69-134">RELATED LINKS</span></span>

[<span data-ttu-id="e2c69-135">Get-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e2c69-135">Get-AzureAutomationVariable</span></span>](./Get-AzureAutomationVariable.md)

[<span data-ttu-id="e2c69-136">Remove-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e2c69-136">Remove-AzureAutomationVariable</span></span>](./Remove-AzureAutomationVariable.md)

[<span data-ttu-id="e2c69-137">Set-AzureAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e2c69-137">Set-AzureAutomationVariable</span></span>](./Set-AzureAutomationVariable.md)


