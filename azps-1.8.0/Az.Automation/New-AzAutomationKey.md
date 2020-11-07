---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
ms.openlocfilehash: 1d0587ae9d1d45de4f08b71baa48ebb5e1633a36
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761568"
---
# <span data-ttu-id="1af04-101">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="1af04-101">New-AzAutomationKey</span></span>

## <span data-ttu-id="1af04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1af04-102">SYNOPSIS</span></span>
<span data-ttu-id="1af04-103">Otomasyon hesabı için kayıt anahtarlarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1af04-103">Regenerates registration keys for an Automation account.</span></span>

## <span data-ttu-id="1af04-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1af04-104">SYNTAX</span></span>

```
New-AzAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1af04-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1af04-105">DESCRIPTION</span></span>
<span data-ttu-id="1af04-106">**New-AzAutomationKey** cmdlet 'ı bir Azure Otomasyonu hesabı için kayıt anahtarlarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1af04-106">The **New-AzAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="1af04-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1af04-107">EXAMPLES</span></span>

### <span data-ttu-id="1af04-108">Örnek 1: Otomasyon hesabı için anahtar oluşturma</span><span class="sxs-lookup"><span data-stu-id="1af04-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="1af04-109">Bu komut, ResourceGroup01 adındaki kaynak grubundaki AutomationAccount01 adındaki Azure Otomasyonu hesabının birincil anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1af04-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="1af04-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1af04-110">PARAMETERS</span></span>

### <span data-ttu-id="1af04-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1af04-111">-AutomationAccountName</span></span>
<span data-ttu-id="1af04-112">Bu cmdlet 'in anahtarları yeniden bildirdiği Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1af04-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

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

### <span data-ttu-id="1af04-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1af04-113">-DefaultProfile</span></span>
<span data-ttu-id="1af04-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1af04-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1af04-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="1af04-115">-KeyType</span></span>
<span data-ttu-id="1af04-116">Aracı kayıt anahtarının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1af04-116">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="1af04-117">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="1af04-117">Valid values are:</span></span> 
- <span data-ttu-id="1af04-118">Yararı</span><span class="sxs-lookup"><span data-stu-id="1af04-118">Primary</span></span> 
- <span data-ttu-id="1af04-119">İK</span><span class="sxs-lookup"><span data-stu-id="1af04-119">Secondary</span></span>

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

### <span data-ttu-id="1af04-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1af04-120">-ResourceGroupName</span></span>
<span data-ttu-id="1af04-121">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1af04-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="1af04-122">Bu cmdlet, bu parametrenin belirttiği kaynak grubundaki Otomasyon hesabının anahtarlarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1af04-122">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1af04-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1af04-123">CommonParameters</span></span>
<span data-ttu-id="1af04-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1af04-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1af04-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1af04-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1af04-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1af04-126">INPUTS</span></span>

### <span data-ttu-id="1af04-127">System. String</span><span class="sxs-lookup"><span data-stu-id="1af04-127">System.String</span></span>

## <span data-ttu-id="1af04-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1af04-128">OUTPUTS</span></span>

### <span data-ttu-id="1af04-129">Microsoft. Azure. Commands. Automation. model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="1af04-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="1af04-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1af04-130">NOTES</span></span>

## <span data-ttu-id="1af04-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1af04-131">RELATED LINKS</span></span>
