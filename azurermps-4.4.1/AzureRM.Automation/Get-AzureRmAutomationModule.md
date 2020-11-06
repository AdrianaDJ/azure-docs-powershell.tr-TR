---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationModule.md
ms.openlocfilehash: dcd84c47ff9a6dae06daaf05bde6dd6f4af86553
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591189"
---
# <span data-ttu-id="322d3-101">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="322d3-101">Get-AzureRmAutomationModule</span></span>

## <span data-ttu-id="322d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="322d3-102">SYNOPSIS</span></span>
<span data-ttu-id="322d3-103">Tüm modüller için meta verileri Otomasyon 'dan alır.</span><span class="sxs-lookup"><span data-stu-id="322d3-103">Gets metadata for modules from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="322d3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="322d3-104">SYNTAX</span></span>

### <span data-ttu-id="322d3-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="322d3-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="322d3-106">ByName</span><span class="sxs-lookup"><span data-stu-id="322d3-106">ByName</span></span>
```
Get-AzureRmAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="322d3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="322d3-107">DESCRIPTION</span></span>
<span data-ttu-id="322d3-108">**Get-AzureRmAutomationModule** cmdlet 'ı Azure Otomasyonu 'ndan alınan modüller için meta verileri alır.</span><span class="sxs-lookup"><span data-stu-id="322d3-108">The **Get-AzureRmAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="322d3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="322d3-109">EXAMPLES</span></span>

### <span data-ttu-id="322d3-110">Örnek 1: tüm modülleri al</span><span class="sxs-lookup"><span data-stu-id="322d3-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzureRmAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="322d3-111">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm modülleri alır.</span><span class="sxs-lookup"><span data-stu-id="322d3-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="322d3-112">Örnek 2: modül alma</span><span class="sxs-lookup"><span data-stu-id="322d3-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="322d3-113">Bu komut, Contoso17 adlı Otomasyon hesabında ContosoModule adlı bir modül alır.</span><span class="sxs-lookup"><span data-stu-id="322d3-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="322d3-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="322d3-114">PARAMETERS</span></span>

### <span data-ttu-id="322d3-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="322d3-115">-AutomationAccountName</span></span>
<span data-ttu-id="322d3-116">Bu cmdlet 'in modül meta verilerini aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="322d3-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="322d3-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="322d3-117">-Name</span></span>
<span data-ttu-id="322d3-118">Bu cmdlet 'in meta veri aldığı modülün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="322d3-118">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="322d3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="322d3-119">-ResourceGroupName</span></span>
<span data-ttu-id="322d3-120">Bu cmdlet 'in modül meta verilerini aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="322d3-120">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="322d3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="322d3-121">-DefaultProfile</span></span>
<span data-ttu-id="322d3-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="322d3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="322d3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="322d3-123">CommonParameters</span></span>
<span data-ttu-id="322d3-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="322d3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="322d3-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="322d3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="322d3-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="322d3-126">INPUTS</span></span>

## <span data-ttu-id="322d3-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="322d3-127">OUTPUTS</span></span>

### <span data-ttu-id="322d3-128">Microsoft. Azure. Commands. Automation. model. Module</span><span class="sxs-lookup"><span data-stu-id="322d3-128">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="322d3-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="322d3-129">NOTES</span></span>

## <span data-ttu-id="322d3-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="322d3-130">RELATED LINKS</span></span>

[<span data-ttu-id="322d3-131">Yeni-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="322d3-131">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="322d3-132">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="322d3-132">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)

[<span data-ttu-id="322d3-133">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="322d3-133">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


