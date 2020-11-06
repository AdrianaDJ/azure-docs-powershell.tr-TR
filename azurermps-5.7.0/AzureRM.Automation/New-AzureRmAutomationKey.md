---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationKey.md
ms.openlocfilehash: 0f8cbf67af4cc62c5cdeaae216a2c0a63cbe5afc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594501"
---
# <span data-ttu-id="03643-101">New-AzureRmAutomationKey</span><span class="sxs-lookup"><span data-stu-id="03643-101">New-AzureRmAutomationKey</span></span>

## <span data-ttu-id="03643-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03643-102">SYNOPSIS</span></span>
<span data-ttu-id="03643-103">Otomasyon hesabı için kayıt anahtarlarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="03643-103">Regenerates registration keys for an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03643-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="03643-104">SYNTAX</span></span>

```
New-AzureRmAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03643-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="03643-105">DESCRIPTION</span></span>
<span data-ttu-id="03643-106">**Yeni-AzureRmAutomationKey** cmdlet 'ı bir Azure Otomasyonu hesabının kayıt anahtarlarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="03643-106">The **New-AzureRmAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="03643-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="03643-107">EXAMPLES</span></span>

### <span data-ttu-id="03643-108">Örnek 1: Otomasyon hesabı için anahtar oluşturma</span><span class="sxs-lookup"><span data-stu-id="03643-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzureAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="03643-109">Bu komut, ResourceGroup01 adındaki kaynak grubundaki AutomationAccount01 adındaki Azure Otomasyonu hesabının birincil anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="03643-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="03643-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="03643-110">PARAMETERS</span></span>

### <span data-ttu-id="03643-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="03643-111">-AutomationAccountName</span></span>
<span data-ttu-id="03643-112">Bu cmdlet 'in anahtarları yeniden bildirdiği Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="03643-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03643-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03643-113">-DefaultProfile</span></span>
<span data-ttu-id="03643-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="03643-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03643-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="03643-115">-KeyType</span></span>
<span data-ttu-id="03643-116">Aracı kayıt anahtarının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="03643-116">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="03643-117">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="03643-117">Valid values are:</span></span> 

- <span data-ttu-id="03643-118">Yararı</span><span class="sxs-lookup"><span data-stu-id="03643-118">Primary</span></span> 
- <span data-ttu-id="03643-119">İK</span><span class="sxs-lookup"><span data-stu-id="03643-119">Secondary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03643-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03643-120">-ResourceGroupName</span></span>
<span data-ttu-id="03643-121">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="03643-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="03643-122">Bu cmdlet, bu parametrenin belirttiği kaynak grubundaki Otomasyon hesabının anahtarlarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="03643-122">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03643-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03643-123">CommonParameters</span></span>
<span data-ttu-id="03643-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="03643-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03643-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03643-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03643-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="03643-126">INPUTS</span></span>

### <span data-ttu-id="03643-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="03643-127">None</span></span>
<span data-ttu-id="03643-128">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="03643-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="03643-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="03643-129">OUTPUTS</span></span>

### <span data-ttu-id="03643-130">Microsoft. Azure. Commands. Automation. model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="03643-130">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="03643-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="03643-131">NOTES</span></span>

## <span data-ttu-id="03643-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="03643-132">RELATED LINKS</span></span>

