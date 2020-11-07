---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
ms.openlocfilehash: f915d1637226e7381cf7da53c0a3aea022060be1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753317"
---
# <span data-ttu-id="dc5e4-101">Get-AzAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="dc5e4-101">Get-AzAutomationRegistrationInfo</span></span>

## <span data-ttu-id="dc5e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc5e4-102">SYNOPSIS</span></span>
<span data-ttu-id="dc5e4-103">DSC düğümünü veya karma çalışanı otomatikleştirme 'ye eklemek için kayıt bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="dc5e4-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

## <span data-ttu-id="dc5e4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dc5e4-104">SYNTAX</span></span>

```
Get-AzAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc5e4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dc5e4-105">DESCRIPTION</span></span>
<span data-ttu-id="dc5e4-106">**Get-Azautomationregistrationınfo** cmdlet 'ı, Istenen durum YAPıLANDıRMASı (DSC) düğümünü veya karma çalışanı bir Azure Otomasyonu hesabına eklemek için gereken uç nokta ve anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="dc5e4-106">The **Get-AzAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="dc5e4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dc5e4-107">EXAMPLES</span></span>

### <span data-ttu-id="dc5e4-108">Örnek 1: kayıt bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="dc5e4-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="dc5e4-109">Bu komut, ResourceGroup01 adındaki kaynak grubundaki AutomationAccount01 adındaki Otomasyon hesabının kayıt bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="dc5e4-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="dc5e4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dc5e4-110">PARAMETERS</span></span>

### <span data-ttu-id="dc5e4-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dc5e4-111">-AutomationAccountName</span></span>
<span data-ttu-id="dc5e4-112">Bu cmdlet 'in kayıt bilgilerini aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dc5e4-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

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

### <span data-ttu-id="dc5e4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc5e4-113">-DefaultProfile</span></span>
<span data-ttu-id="dc5e4-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="dc5e4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc5e4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc5e4-115">-ResourceGroupName</span></span>
<span data-ttu-id="dc5e4-116">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dc5e4-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="dc5e4-117">Bu cmdlet, bu parametrenin belirttiği kaynak grubunun kayıt bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="dc5e4-117">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="dc5e4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc5e4-118">CommonParameters</span></span>
<span data-ttu-id="dc5e4-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dc5e4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc5e4-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc5e4-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc5e4-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dc5e4-121">INPUTS</span></span>

### <span data-ttu-id="dc5e4-122">System. String</span><span class="sxs-lookup"><span data-stu-id="dc5e4-122">System.String</span></span>

## <span data-ttu-id="dc5e4-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dc5e4-123">OUTPUTS</span></span>

### <span data-ttu-id="dc5e4-124">Microsoft. Azure. Commands. Automation. model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="dc5e4-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="dc5e4-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dc5e4-125">NOTES</span></span>

## <span data-ttu-id="dc5e4-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dc5e4-126">RELATED LINKS</span></span>

[<span data-ttu-id="dc5e4-127">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="dc5e4-127">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="dc5e4-128">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="dc5e4-128">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="dc5e4-129">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="dc5e4-129">New-AzAutomationKey</span></span>](./New-AzAutomationKey.md)

