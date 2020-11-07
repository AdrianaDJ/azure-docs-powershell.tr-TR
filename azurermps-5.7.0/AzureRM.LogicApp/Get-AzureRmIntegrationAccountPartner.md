---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 6E84E26F-8150-41F8-8823-CEED05619A75
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: 7063fb81705a14f1c1d8f0d02a2dc51d8a5617ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763270"
---
# <span data-ttu-id="ba92e-101">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="ba92e-101">Get-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="ba92e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba92e-102">SYNOPSIS</span></span>
<span data-ttu-id="ba92e-103">Tümleştirme hesabı ortaklarını alır.</span><span class="sxs-lookup"><span data-stu-id="ba92e-103">Gets integration account partners.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba92e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ba92e-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountPartner [-ResourceGroupName <String>] [-Name <String>] [-PartnerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba92e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ba92e-105">DESCRIPTION</span></span>
<span data-ttu-id="ba92e-106">**Get-AzureRmIntegrationAccountPartner** cmdlet 'i, bir kaynak grubundan tümleştirme hesabı ortaklarını alır.</span><span class="sxs-lookup"><span data-stu-id="ba92e-106">The **Get-AzureRmIntegrationAccountPartner** cmdlet gets integration account partners from a resource group.</span></span>
<span data-ttu-id="ba92e-107">Tümleştirme hesap adını, kaynak grubu adını ve ortak adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="ba92e-107">Specify the integration account name, resource group name, and partner name.</span></span>

<span data-ttu-id="ba92e-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="ba92e-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ba92e-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="ba92e-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ba92e-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="ba92e-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ba92e-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="ba92e-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ba92e-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ba92e-112">EXAMPLES</span></span>

### <span data-ttu-id="ba92e-113">Örnek 1: Tümleştirme hesabı ortağı alma</span><span class="sxs-lookup"><span data-stu-id="ba92e-113">Example 1: Get an integration account partner</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="ba92e-114">Bu komut, IntegrationAccountPartner22 adlı tümleştirme hesabı ortağını alır.</span><span class="sxs-lookup"><span data-stu-id="ba92e-114">This command gets the integration account partner named IntegrationAccountPartner22.</span></span>

### <span data-ttu-id="ba92e-115">Örnek 2: Tümleştirme hesabı ortakları kullanarak bir tümleştirme hesabı ortakları alma</span><span class="sxs-lookup"><span data-stu-id="ba92e-115">Example 2: Get an integration account partners by using an integration account name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="ba92e-116">Bu komut, IntegrationAccount31 adlı tümleştirme hesabı için tümleştirme hesabı ortaklarını alır.</span><span class="sxs-lookup"><span data-stu-id="ba92e-116">This command gets the integration account partners for the integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="ba92e-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ba92e-117">PARAMETERS</span></span>

### <span data-ttu-id="ba92e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba92e-118">-DefaultProfile</span></span>
<span data-ttu-id="ba92e-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ba92e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba92e-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="ba92e-120">-Name</span></span>
<span data-ttu-id="ba92e-121">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba92e-121">Specifies the name of an integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba92e-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="ba92e-122">-PartnerName</span></span>
<span data-ttu-id="ba92e-123">Tümleştirme hesap ortağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba92e-123">Specifies the name of the integration account partner.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba92e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba92e-124">-ResourceGroupName</span></span>
<span data-ttu-id="ba92e-125">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba92e-125">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba92e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba92e-126">CommonParameters</span></span>
<span data-ttu-id="ba92e-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ba92e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba92e-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba92e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba92e-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ba92e-129">INPUTS</span></span>

### <span data-ttu-id="ba92e-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ba92e-130">None</span></span>
<span data-ttu-id="ba92e-131">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="ba92e-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ba92e-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ba92e-132">OUTPUTS</span></span>

### <span data-ttu-id="ba92e-133">Microsoft. Azure. Management. Logic. modeller. ıntegrationaccountpartner</span><span class="sxs-lookup"><span data-stu-id="ba92e-133">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="ba92e-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ba92e-134">NOTES</span></span>

## <span data-ttu-id="ba92e-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ba92e-135">RELATED LINKS</span></span>

[<span data-ttu-id="ba92e-136">Yeni-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="ba92e-136">New-AzureRmIntegrationAccountPartner</span></span>](./New-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="ba92e-137">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="ba92e-137">Remove-AzureRmIntegrationAccountPartner</span></span>](./Remove-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="ba92e-138">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="ba92e-138">Set-AzureRmIntegrationAccountPartner</span></span>](./Set-AzureRmIntegrationAccountPartner.md)


