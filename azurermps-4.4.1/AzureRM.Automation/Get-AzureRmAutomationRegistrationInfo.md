---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationRegistrationInfo.md
ms.openlocfilehash: 2ab7feb754bce7b160bf5aa47e225160649a70ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591188"
---
# <span data-ttu-id="76d48-101">Get-AzureRmAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="76d48-101">Get-AzureRmAutomationRegistrationInfo</span></span>

## <span data-ttu-id="76d48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76d48-102">SYNOPSIS</span></span>
<span data-ttu-id="76d48-103">DSC düğümünü veya karma çalışanı otomatikleştirme 'ye eklemek için kayıt bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="76d48-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76d48-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76d48-104">SYNTAX</span></span>

```
Get-AzureRmAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76d48-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="76d48-105">DESCRIPTION</span></span>
<span data-ttu-id="76d48-106">**Get-Azurermautomationregistrationınfo** cmdlet 'ı, Istenen durum YAPıLANDıRMASı (DSC) düğümünü veya karma çalışanı bir Azure Otomasyonu hesabına eklemek için gereken uç nokta ve anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="76d48-106">The **Get-AzureRmAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="76d48-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76d48-107">EXAMPLES</span></span>

### <span data-ttu-id="76d48-108">Örnek 1: kayıt bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="76d48-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzureRmAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="76d48-109">Bu komut, ResourceGroup01 adındaki kaynak grubundaki AutomationAccount01 adındaki Otomasyon hesabının kayıt bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="76d48-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="76d48-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76d48-110">PARAMETERS</span></span>

### <span data-ttu-id="76d48-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="76d48-111">-AutomationAccountName</span></span>
<span data-ttu-id="76d48-112">Bu cmdlet 'in kayıt bilgilerini aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="76d48-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

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

### <span data-ttu-id="76d48-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76d48-113">-ResourceGroupName</span></span>
<span data-ttu-id="76d48-114">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="76d48-114">Specifies the name of a resource group.</span></span>
<span data-ttu-id="76d48-115">Bu cmdlet, bu parametrenin belirttiği kaynak grubunun kayıt bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="76d48-115">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="76d48-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76d48-116">-DefaultProfile</span></span>
<span data-ttu-id="76d48-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="76d48-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76d48-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76d48-118">CommonParameters</span></span>
<span data-ttu-id="76d48-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76d48-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76d48-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76d48-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76d48-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76d48-121">INPUTS</span></span>

## <span data-ttu-id="76d48-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76d48-122">OUTPUTS</span></span>

### <span data-ttu-id="76d48-123">Microsoft. Azure. Commands. Automation. model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="76d48-123">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="76d48-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76d48-124">NOTES</span></span>

## <span data-ttu-id="76d48-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76d48-125">RELATED LINKS</span></span>

[<span data-ttu-id="76d48-126">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="76d48-126">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="76d48-127">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="76d48-127">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="76d48-128">Yeni-AzureRmAutomationKey</span><span class="sxs-lookup"><span data-stu-id="76d48-128">New-AzureRmAutomationKey</span></span>](./New-AzureRmAutomationKey.md)

