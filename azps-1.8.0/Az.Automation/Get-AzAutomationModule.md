---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
ms.openlocfilehash: 54bbda0226cf2aa374e149bc4b5885b86b31ef12
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761610"
---
# <span data-ttu-id="46185-101">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="46185-101">Get-AzAutomationModule</span></span>

## <span data-ttu-id="46185-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46185-102">SYNOPSIS</span></span>
<span data-ttu-id="46185-103">Tüm modüller için meta verileri Otomasyon 'dan alır.</span><span class="sxs-lookup"><span data-stu-id="46185-103">Gets metadata for modules from Automation.</span></span>

## <span data-ttu-id="46185-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="46185-104">SYNTAX</span></span>

### <span data-ttu-id="46185-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="46185-105">ByAll (Default)</span></span>
```
Get-AzAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46185-106">ByName</span><span class="sxs-lookup"><span data-stu-id="46185-106">ByName</span></span>
```
Get-AzAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46185-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="46185-107">DESCRIPTION</span></span>
<span data-ttu-id="46185-108">**Get-AzAutomationModule** cmdlet 'ı Azure Automation 'daki modüller için meta verileri alır.</span><span class="sxs-lookup"><span data-stu-id="46185-108">The **Get-AzAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="46185-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="46185-109">EXAMPLES</span></span>

### <span data-ttu-id="46185-110">Örnek 1: tüm modülleri al</span><span class="sxs-lookup"><span data-stu-id="46185-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="46185-111">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm modülleri alır.</span><span class="sxs-lookup"><span data-stu-id="46185-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="46185-112">Örnek 2: modül alma</span><span class="sxs-lookup"><span data-stu-id="46185-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="46185-113">Bu komut, Contoso17 adlı Otomasyon hesabında ContosoModule adlı bir modül alır.</span><span class="sxs-lookup"><span data-stu-id="46185-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="46185-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="46185-114">PARAMETERS</span></span>

### <span data-ttu-id="46185-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="46185-115">-AutomationAccountName</span></span>
<span data-ttu-id="46185-116">Bu cmdlet 'in modül meta verilerini aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46185-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="46185-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46185-117">-DefaultProfile</span></span>
<span data-ttu-id="46185-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="46185-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46185-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="46185-119">-Name</span></span>
<span data-ttu-id="46185-120">Bu cmdlet 'in meta veri aldığı modülün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46185-120">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="46185-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46185-121">-ResourceGroupName</span></span>
<span data-ttu-id="46185-122">Bu cmdlet 'in modül meta verilerini aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46185-122">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="46185-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46185-123">CommonParameters</span></span>
<span data-ttu-id="46185-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="46185-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46185-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46185-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46185-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="46185-126">INPUTS</span></span>

### <span data-ttu-id="46185-127">System. String</span><span class="sxs-lookup"><span data-stu-id="46185-127">System.String</span></span>

## <span data-ttu-id="46185-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="46185-128">OUTPUTS</span></span>

### <span data-ttu-id="46185-129">Microsoft. Azure. Commands. Automation. model. Module</span><span class="sxs-lookup"><span data-stu-id="46185-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="46185-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="46185-130">NOTES</span></span>

## <span data-ttu-id="46185-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="46185-131">RELATED LINKS</span></span>

[<span data-ttu-id="46185-132">Yeni-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="46185-132">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="46185-133">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="46185-133">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="46185-134">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="46185-134">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


