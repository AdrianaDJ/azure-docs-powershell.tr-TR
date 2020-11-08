---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
ms.openlocfilehash: ed10bd42fb52515cb05adadfc69ee4f1620150e3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104969"
---
# <span data-ttu-id="e9eb3-101">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="e9eb3-101">New-AzAutomationKey</span></span>

## <span data-ttu-id="e9eb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9eb3-102">SYNOPSIS</span></span>
<span data-ttu-id="e9eb3-103">Otomasyon hesabı için kayıt anahtarlarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e9eb3-103">Regenerates registration keys for an Automation account.</span></span>

## <span data-ttu-id="e9eb3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e9eb3-104">SYNTAX</span></span>

```
New-AzAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9eb3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e9eb3-105">DESCRIPTION</span></span>
<span data-ttu-id="e9eb3-106">**New-AzAutomationKey** cmdlet 'ı bir Azure Otomasyonu hesabı için kayıt anahtarlarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e9eb3-106">The **New-AzAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="e9eb3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e9eb3-107">EXAMPLES</span></span>

### <span data-ttu-id="e9eb3-108">Örnek 1: Otomasyon hesabı için anahtar oluşturma</span><span class="sxs-lookup"><span data-stu-id="e9eb3-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="e9eb3-109">Bu komut, ResourceGroup01 adındaki kaynak grubundaki AutomationAccount01 adındaki Azure Otomasyonu hesabının birincil anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e9eb3-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="e9eb3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e9eb3-110">PARAMETERS</span></span>

### <span data-ttu-id="e9eb3-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e9eb3-111">-AutomationAccountName</span></span>
<span data-ttu-id="e9eb3-112">Bu cmdlet 'in anahtarları yeniden bildirdiği Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9eb3-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

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

### <span data-ttu-id="e9eb3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9eb3-113">-DefaultProfile</span></span>
<span data-ttu-id="e9eb3-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e9eb3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9eb3-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="e9eb3-115">-KeyType</span></span>
<span data-ttu-id="e9eb3-116">Aracı kayıt anahtarının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9eb3-116">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="e9eb3-117">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="e9eb3-117">Valid values are:</span></span> 
- <span data-ttu-id="e9eb3-118">Yararı</span><span class="sxs-lookup"><span data-stu-id="e9eb3-118">Primary</span></span> 
- <span data-ttu-id="e9eb3-119">İK</span><span class="sxs-lookup"><span data-stu-id="e9eb3-119">Secondary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9eb3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9eb3-120">-ResourceGroupName</span></span>
<span data-ttu-id="e9eb3-121">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9eb3-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="e9eb3-122">Bu cmdlet, bu parametrenin belirttiği kaynak grubundaki Otomasyon hesabının anahtarlarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e9eb3-122">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e9eb3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9eb3-123">CommonParameters</span></span>
<span data-ttu-id="e9eb3-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e9eb3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9eb3-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9eb3-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9eb3-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e9eb3-126">INPUTS</span></span>

### <span data-ttu-id="e9eb3-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e9eb3-127">System.String</span></span>

## <span data-ttu-id="e9eb3-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e9eb3-128">OUTPUTS</span></span>

### <span data-ttu-id="e9eb3-129">Microsoft. Azure. Commands. Automation. model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="e9eb3-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="e9eb3-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e9eb3-130">NOTES</span></span>

## <span data-ttu-id="e9eb3-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e9eb3-131">RELATED LINKS</span></span>
