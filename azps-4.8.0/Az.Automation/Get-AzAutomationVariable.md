---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 8FB78A4A-8392-44EE-A907-10FDF756071B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
ms.openlocfilehash: a8238cf9de2b0b20cb347d16bb74623f6469c03c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109217"
---
# <span data-ttu-id="1e027-101">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="1e027-101">Get-AzAutomationVariable</span></span>

## <span data-ttu-id="1e027-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e027-102">SYNOPSIS</span></span>
<span data-ttu-id="1e027-103">Bir Otomasyon değişkeni alır.</span><span class="sxs-lookup"><span data-stu-id="1e027-103">Gets an Automation variable.</span></span>

## <span data-ttu-id="1e027-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1e027-104">SYNTAX</span></span>

### <span data-ttu-id="1e027-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1e027-105">ByAll (Default)</span></span>
```
Get-AzAutomationVariable [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e027-106">ByName</span><span class="sxs-lookup"><span data-stu-id="1e027-106">ByName</span></span>
```
Get-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e027-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1e027-107">DESCRIPTION</span></span>
<span data-ttu-id="1e027-108">**Get-AzAutomationVariable** cmdlet 'i bir veya birden çok Azure Otomasyonu değişkenini alır.</span><span class="sxs-lookup"><span data-stu-id="1e027-108">The **Get-AzAutomationVariable** cmdlet gets one or more Azure Automation variables.</span></span>
<span data-ttu-id="1e027-109">Belirli bir değişken almak için adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="1e027-109">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="1e027-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1e027-110">EXAMPLES</span></span>

### <span data-ttu-id="1e027-111">Örnek 1: değişken alma</span><span class="sxs-lookup"><span data-stu-id="1e027-111">Example 1: Get a variable</span></span>
```
PS C:\>$Variable = Get-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "Variable06" -ResourceGroupName "ResourceGroup01"
PS C:\> $Value = $Variable.value
```

<span data-ttu-id="1e027-112">İlk komut, Contoso17 adlı hesapta Variable06 adlı bir Otomasyon değişkeni alır.</span><span class="sxs-lookup"><span data-stu-id="1e027-112">The first command gets an Automation variable named Variable06 in the account named Contoso17.</span></span>
<span data-ttu-id="1e027-113">Komut bu nesneyi $Variable değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="1e027-113">The command stores that object in the $Variable variable.</span></span>
<span data-ttu-id="1e027-114">İkinci komut, $Variable **değer** özelliğine başvuruda bulunmak için standart nokta gösterimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="1e027-114">The second command uses standard dot notation to refer to the **value** property of $Variable.</span></span>
<span data-ttu-id="1e027-115">Komut $value değişkeninde değeri depolar.</span><span class="sxs-lookup"><span data-stu-id="1e027-115">The command stores the value in the $value variable.</span></span>

## <span data-ttu-id="1e027-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1e027-116">PARAMETERS</span></span>

### <span data-ttu-id="1e027-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1e027-117">-AutomationAccountName</span></span>
<span data-ttu-id="1e027-118">Bu cmdlet 'in aldığı değişkenleri içeren Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e027-118">Specifies the name of the Automation account that contains the variables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1e027-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e027-119">-DefaultProfile</span></span>
<span data-ttu-id="1e027-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1e027-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e027-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="1e027-121">-Name</span></span>
<span data-ttu-id="1e027-122">Bu cmdlet 'in aldığı değişkenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e027-122">Specifies the name of a variable that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1e027-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e027-123">-ResourceGroupName</span></span>
<span data-ttu-id="1e027-124">Bu cmdlet 'in değişkenleri aldığı kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e027-124">Specifies the resource group for which this cmdlet gets variables.</span></span>

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

### <span data-ttu-id="1e027-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e027-125">CommonParameters</span></span>
<span data-ttu-id="1e027-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1e027-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e027-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e027-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e027-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1e027-128">INPUTS</span></span>

### <span data-ttu-id="1e027-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1e027-129">System.String</span></span>

## <span data-ttu-id="1e027-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1e027-130">OUTPUTS</span></span>

### <span data-ttu-id="1e027-131">Microsoft. Azure. Commands. Automation. model. Variable</span><span class="sxs-lookup"><span data-stu-id="1e027-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="1e027-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1e027-132">NOTES</span></span>

## <span data-ttu-id="1e027-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1e027-133">RELATED LINKS</span></span>

[<span data-ttu-id="1e027-134">Yeni-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="1e027-134">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="1e027-135">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="1e027-135">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="1e027-136">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="1e027-136">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


