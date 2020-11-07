---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 8FB78A4A-8392-44EE-A907-10FDF756071B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationVariable.md
ms.openlocfilehash: 3eecca08264b83ac46b0927273ff07149d4cc348
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763410"
---
# <span data-ttu-id="6a51a-101">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="6a51a-101">Get-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="6a51a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a51a-102">SYNOPSIS</span></span>
<span data-ttu-id="6a51a-103">Bir Otomasyon değişkeni alır.</span><span class="sxs-lookup"><span data-stu-id="6a51a-103">Gets an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a51a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6a51a-104">SYNTAX</span></span>

### <span data-ttu-id="6a51a-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6a51a-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationVariable [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a51a-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6a51a-106">ByName</span></span>
```
Get-AzureRmAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a51a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6a51a-107">DESCRIPTION</span></span>
<span data-ttu-id="6a51a-108">**Get-AzureRmAutomationVariable** cmdlet 'i bir veya birden çok Azure Otomasyonu değişkenini alır.</span><span class="sxs-lookup"><span data-stu-id="6a51a-108">The **Get-AzureRmAutomationVariable** cmdlet gets one or more Azure Automation variables.</span></span>
<span data-ttu-id="6a51a-109">Belirli bir değişken almak için adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="6a51a-109">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="6a51a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6a51a-110">EXAMPLES</span></span>

### <span data-ttu-id="6a51a-111">Örnek 1: değişken alma</span><span class="sxs-lookup"><span data-stu-id="6a51a-111">Example 1: Get a variable</span></span>
```
PS C:\>$Variable = Get-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "Variable06" -ResourceGroupName "ResourceGroup01"
PS C:\> $Value = $Variable.value
```

<span data-ttu-id="6a51a-112">İlk komut, Contoso17 adlı hesapta Variable06 adlı bir Otomasyon değişkeni alır.</span><span class="sxs-lookup"><span data-stu-id="6a51a-112">The first command gets an Automation variable named Variable06 in the account named Contoso17.</span></span>
<span data-ttu-id="6a51a-113">Komut bu nesneyi $Variable değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6a51a-113">The command stores that object in the $Variable variable.</span></span>

<span data-ttu-id="6a51a-114">İkinci komut, $Variable **değer** özelliğine başvuruda bulunmak için standart nokta gösterimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="6a51a-114">The second command uses standard dot notation to refer to the **value** property of $Variable.</span></span>
<span data-ttu-id="6a51a-115">Komut $value değişkeninde değeri depolar.</span><span class="sxs-lookup"><span data-stu-id="6a51a-115">The command stores the value in the $value variable.</span></span>

## <span data-ttu-id="6a51a-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6a51a-116">PARAMETERS</span></span>

### <span data-ttu-id="6a51a-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6a51a-117">-AutomationAccountName</span></span>
<span data-ttu-id="6a51a-118">Bu cmdlet 'in aldığı değişkenleri içeren Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a51a-118">Specifies the name of the Automation account that contains the variables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6a51a-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="6a51a-119">-Name</span></span>
<span data-ttu-id="6a51a-120">Bu cmdlet 'in aldığı değişkenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a51a-120">Specifies the name of a variable that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a51a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a51a-121">-ResourceGroupName</span></span>
<span data-ttu-id="6a51a-122">Bu cmdlet 'in değişkenleri aldığı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a51a-122">Specifies the resource group for which this cmdlet gets variables.</span></span>

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

### <span data-ttu-id="6a51a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a51a-123">-DefaultProfile</span></span>
<span data-ttu-id="6a51a-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6a51a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a51a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a51a-125">CommonParameters</span></span>
<span data-ttu-id="6a51a-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6a51a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a51a-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a51a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a51a-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6a51a-128">INPUTS</span></span>

## <span data-ttu-id="6a51a-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6a51a-129">OUTPUTS</span></span>

### <span data-ttu-id="6a51a-130">Microsoft. Azure. Commands. Automation. model. Variable</span><span class="sxs-lookup"><span data-stu-id="6a51a-130">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="6a51a-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6a51a-131">NOTES</span></span>

## <span data-ttu-id="6a51a-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6a51a-132">RELATED LINKS</span></span>

[<span data-ttu-id="6a51a-133">Yeni-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="6a51a-133">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="6a51a-134">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="6a51a-134">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)

[<span data-ttu-id="6a51a-135">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="6a51a-135">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


