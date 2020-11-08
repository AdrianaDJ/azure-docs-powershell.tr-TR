---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6E84E26F-8150-41F8-8823-CEED05619A75
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
ms.openlocfilehash: cf6d2f4da1803e5c9403803ea7231b55c13d7243
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109577"
---
# <span data-ttu-id="65501-101">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="65501-101">Get-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="65501-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65501-102">SYNOPSIS</span></span>
<span data-ttu-id="65501-103">Tümleştirme hesabı ortaklarını alır.</span><span class="sxs-lookup"><span data-stu-id="65501-103">Gets integration account partners.</span></span>

## <span data-ttu-id="65501-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="65501-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountPartner [-ResourceGroupName <String>] [-Name <String>] [-PartnerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65501-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="65501-105">DESCRIPTION</span></span>
<span data-ttu-id="65501-106">**Get-Azıntegrationaccountpartner** cmdlet 'i bir kaynak grubundan tümleştirme hesabı ortaklarını alır.</span><span class="sxs-lookup"><span data-stu-id="65501-106">The **Get-AzIntegrationAccountPartner** cmdlet gets integration account partners from a resource group.</span></span>
<span data-ttu-id="65501-107">Tümleştirme hesap adını, kaynak grubu adını ve ortak adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="65501-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="65501-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="65501-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="65501-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="65501-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="65501-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="65501-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="65501-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="65501-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="65501-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="65501-112">EXAMPLES</span></span>

### <span data-ttu-id="65501-113">Örnek 1: Tümleştirme hesabı ortağı alma</span><span class="sxs-lookup"><span data-stu-id="65501-113">Example 1: Get an integration account partner</span></span>
```
PS C:\>Get-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="65501-114">Bu komut, IntegrationAccountPartner22 adlı tümleştirme hesabı ortağını alır.</span><span class="sxs-lookup"><span data-stu-id="65501-114">This command gets the integration account partner named IntegrationAccountPartner22.</span></span>

### <span data-ttu-id="65501-115">Örnek 2: Tümleştirme hesabı ortakları kullanarak bir tümleştirme hesabı ortakları alma</span><span class="sxs-lookup"><span data-stu-id="65501-115">Example 2: Get an integration account partners by using an integration account name</span></span>
```
PS C:\>Get-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="65501-116">Bu komut, IntegrationAccount31 adlı tümleştirme hesabı için tümleştirme hesabı ortaklarını alır.</span><span class="sxs-lookup"><span data-stu-id="65501-116">This command gets the integration account partners for the integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="65501-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="65501-117">PARAMETERS</span></span>

### <span data-ttu-id="65501-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65501-118">-DefaultProfile</span></span>
<span data-ttu-id="65501-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="65501-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65501-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="65501-120">-Name</span></span>
<span data-ttu-id="65501-121">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="65501-121">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65501-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="65501-122">-PartnerName</span></span>
<span data-ttu-id="65501-123">Tümleştirme hesap ortağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="65501-123">Specifies the name of the integration account partner.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65501-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65501-124">-ResourceGroupName</span></span>
<span data-ttu-id="65501-125">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="65501-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65501-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65501-126">CommonParameters</span></span>
<span data-ttu-id="65501-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="65501-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65501-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65501-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65501-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="65501-129">INPUTS</span></span>

### <span data-ttu-id="65501-130">System. String</span><span class="sxs-lookup"><span data-stu-id="65501-130">System.String</span></span>

## <span data-ttu-id="65501-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="65501-131">OUTPUTS</span></span>

### <span data-ttu-id="65501-132">Microsoft. Azure. Management. Logic. modeller. ıntegrationaccountpartner</span><span class="sxs-lookup"><span data-stu-id="65501-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="65501-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="65501-133">NOTES</span></span>

## <span data-ttu-id="65501-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="65501-134">RELATED LINKS</span></span>

[<span data-ttu-id="65501-135">Yeni-az</span><span class="sxs-lookup"><span data-stu-id="65501-135">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="65501-136">Remove-Azıntegrationaccountpartner</span><span class="sxs-lookup"><span data-stu-id="65501-136">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)

[<span data-ttu-id="65501-137">Set-Azıntegrationaccountpartner</span><span class="sxs-lookup"><span data-stu-id="65501-137">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


