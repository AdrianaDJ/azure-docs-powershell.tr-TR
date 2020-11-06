---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationRegistrationInfo.md
ms.openlocfilehash: 84332967eadfdb2accd12cc2f6f840ee337f92ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587315"
---
# <span data-ttu-id="3b5ae-101">Get-AzureRmAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="3b5ae-101">Get-AzureRmAutomationRegistrationInfo</span></span>

## <span data-ttu-id="3b5ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b5ae-102">SYNOPSIS</span></span>
<span data-ttu-id="3b5ae-103">DSC düğümünü veya karma çalışanı otomatikleştirme 'ye eklemek için kayıt bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="3b5ae-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b5ae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3b5ae-104">SYNTAX</span></span>

```
Get-AzureRmAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b5ae-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3b5ae-105">DESCRIPTION</span></span>
<span data-ttu-id="3b5ae-106">**Get-Azurermautomationregistrationınfo** cmdlet 'ı, Istenen durum YAPıLANDıRMASı (DSC) düğümünü veya karma çalışanı bir Azure Otomasyonu hesabına eklemek için gereken uç nokta ve anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="3b5ae-106">The **Get-AzureRmAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="3b5ae-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3b5ae-107">EXAMPLES</span></span>

### <span data-ttu-id="3b5ae-108">Örnek 1: kayıt bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="3b5ae-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzureRmAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="3b5ae-109">Bu komut, ResourceGroup01 adındaki kaynak grubundaki AutomationAccount01 adındaki Otomasyon hesabının kayıt bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="3b5ae-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="3b5ae-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3b5ae-110">PARAMETERS</span></span>

### <span data-ttu-id="3b5ae-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3b5ae-111">-AutomationAccountName</span></span>
<span data-ttu-id="3b5ae-112">Bu cmdlet 'in kayıt bilgilerini aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b5ae-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

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

### <span data-ttu-id="3b5ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b5ae-113">-DefaultProfile</span></span>
<span data-ttu-id="3b5ae-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3b5ae-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b5ae-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b5ae-115">-ResourceGroupName</span></span>
<span data-ttu-id="3b5ae-116">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b5ae-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="3b5ae-117">Bu cmdlet, bu parametrenin belirttiği kaynak grubunun kayıt bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="3b5ae-117">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3b5ae-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b5ae-118">CommonParameters</span></span>
<span data-ttu-id="3b5ae-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3b5ae-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b5ae-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b5ae-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b5ae-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3b5ae-121">INPUTS</span></span>

### <span data-ttu-id="3b5ae-122">System. String</span><span class="sxs-lookup"><span data-stu-id="3b5ae-122">System.String</span></span>

## <span data-ttu-id="3b5ae-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3b5ae-123">OUTPUTS</span></span>

### <span data-ttu-id="3b5ae-124">Microsoft. Azure. Commands. Automation. model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="3b5ae-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="3b5ae-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3b5ae-125">NOTES</span></span>

## <span data-ttu-id="3b5ae-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3b5ae-126">RELATED LINKS</span></span>

[<span data-ttu-id="3b5ae-127">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="3b5ae-127">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="3b5ae-128">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="3b5ae-128">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="3b5ae-129">Yeni-AzureRmAutomationKey</span><span class="sxs-lookup"><span data-stu-id="3b5ae-129">New-AzureRmAutomationKey</span></span>](./New-AzureRmAutomationKey.md)


