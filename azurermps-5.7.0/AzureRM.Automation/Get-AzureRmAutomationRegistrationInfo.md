---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationRegistrationInfo.md
ms.openlocfilehash: dfdd4d4de935d83beaa20246c490ded7b23dcc9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586828"
---
# <span data-ttu-id="da682-101">Get-AzureRmAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="da682-101">Get-AzureRmAutomationRegistrationInfo</span></span>

## <span data-ttu-id="da682-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da682-102">SYNOPSIS</span></span>
<span data-ttu-id="da682-103">DSC düğümünü veya karma çalışanı otomatikleştirme 'ye eklemek için kayıt bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="da682-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da682-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="da682-104">SYNTAX</span></span>

```
Get-AzureRmAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da682-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="da682-105">DESCRIPTION</span></span>
<span data-ttu-id="da682-106">**Get-Azurermautomationregistrationınfo** cmdlet 'ı, Istenen durum YAPıLANDıRMASı (DSC) düğümünü veya karma çalışanı bir Azure Otomasyonu hesabına eklemek için gereken uç nokta ve anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="da682-106">The **Get-AzureRmAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="da682-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="da682-107">EXAMPLES</span></span>

### <span data-ttu-id="da682-108">Örnek 1: kayıt bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="da682-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzureRmAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="da682-109">Bu komut, ResourceGroup01 adındaki kaynak grubundaki AutomationAccount01 adındaki Otomasyon hesabının kayıt bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="da682-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="da682-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="da682-110">PARAMETERS</span></span>

### <span data-ttu-id="da682-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="da682-111">-AutomationAccountName</span></span>
<span data-ttu-id="da682-112">Bu cmdlet 'in kayıt bilgilerini aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="da682-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

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

### <span data-ttu-id="da682-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da682-113">-DefaultProfile</span></span>
<span data-ttu-id="da682-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="da682-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da682-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da682-115">-ResourceGroupName</span></span>
<span data-ttu-id="da682-116">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="da682-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="da682-117">Bu cmdlet, bu parametrenin belirttiği kaynak grubunun kayıt bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="da682-117">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="da682-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da682-118">CommonParameters</span></span>
<span data-ttu-id="da682-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="da682-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da682-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da682-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da682-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="da682-121">INPUTS</span></span>

### <span data-ttu-id="da682-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="da682-122">None</span></span>
<span data-ttu-id="da682-123">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="da682-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="da682-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="da682-124">OUTPUTS</span></span>

### <span data-ttu-id="da682-125">Microsoft. Azure. Commands. Automation. model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="da682-125">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="da682-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="da682-126">NOTES</span></span>

## <span data-ttu-id="da682-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="da682-127">RELATED LINKS</span></span>

[<span data-ttu-id="da682-128">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="da682-128">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="da682-129">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="da682-129">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="da682-130">Yeni-AzureRmAutomationKey</span><span class="sxs-lookup"><span data-stu-id="da682-130">New-AzureRmAutomationKey</span></span>](./New-AzureRmAutomationKey.md)


