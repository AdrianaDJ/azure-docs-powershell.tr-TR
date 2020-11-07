---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4F65A8B3-A250-41C1-9AA5-DBEB3193C401
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountMap.md
ms.openlocfilehash: 39e78dfc27c325b9327d8ca7c27d800d656e3536
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916088"
---
# <span data-ttu-id="6055f-101">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="6055f-101">Get-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="6055f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6055f-102">SYNOPSIS</span></span>
<span data-ttu-id="6055f-103">Tümleştirme hesabı haritasını alır.</span><span class="sxs-lookup"><span data-stu-id="6055f-103">Gets an integration account map.</span></span>

## <span data-ttu-id="6055f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6055f-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountMap [-ResourceGroupName <String>] [-Name <String>] [-MapName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6055f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6055f-105">DESCRIPTION</span></span>
<span data-ttu-id="6055f-106">**Get-Azıntegrationaccountmap** cmdlet 'i bir kaynak grubundan tümleştirme hesabı haritasını alır.</span><span class="sxs-lookup"><span data-stu-id="6055f-106">The **Get-AzIntegrationAccountMap** cmdlet gets integration account map from a resource group.</span></span>
<span data-ttu-id="6055f-107">Tümleştirme hesap adını, kaynak grubu adını ve harita adını belirtme.</span><span class="sxs-lookup"><span data-stu-id="6055f-107">Specifying the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="6055f-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="6055f-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="6055f-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="6055f-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="6055f-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="6055f-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="6055f-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="6055f-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="6055f-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6055f-112">EXAMPLES</span></span>

### <span data-ttu-id="6055f-113">Örnek 1: Tümleştirme hesabı haritasını alma</span><span class="sxs-lookup"><span data-stu-id="6055f-113">Example 1: Get an integration account map</span></span>
```
PS C:\>Get-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name                 : IntegrationAccountMap47
Type                 : Microsoft.Logic/integrationAccounts/maps
CreatedTime          : 3/24/2016 10:34:26 PM
ChangedTime          : 3/24/2016 10:34:26 PM
MapType              : Xslt
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts8811f0155a364b5e9618ba28f7180601/99D1E_XSLT_INTEGRATIONACCOUNT
                       MAP1-9A960F9B71C844CDB09D4922B3BCFF61?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 3056
Metadata             :
```

<span data-ttu-id="6055f-114">Bu komut, belirtilen kaynak grubundaki IntegrationAccountMap47 adlı bir tümleştirme hesabı haritasını alır.</span><span class="sxs-lookup"><span data-stu-id="6055f-114">This command gets an integration account map named IntegrationAccountMap47 in the specified resource group.</span></span>

### <span data-ttu-id="6055f-115">Örnek 2: Tümleştirme hesabı adlarını tümleştirme hesap adıyla alma</span><span class="sxs-lookup"><span data-stu-id="6055f-115">Example 2: Get integration account maps by integration account name</span></span>
```
PS C:\>Get-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name                 : IntegrationAccountMap47
Type                 : Microsoft.Logic/integrationAccounts/maps
CreatedTime          : 3/24/2016 10:34:26 PM
ChangedTime          : 3/24/2016 10:34:26 PM
MapType              : Xslt
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts8811f0155a364b5e9618ba28f7180601/99D1E_XSLT_INTEGRATIONACCOUNT
                       MAP1-9A960F9B71C844CDB09D4922B3BCFF61?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 3056
Metadata             :
```

<span data-ttu-id="6055f-116">Bu komut Integration Account adını Integration Account Name ile alır.</span><span class="sxs-lookup"><span data-stu-id="6055f-116">This command gets the integration account maps by integration account name.</span></span>

## <span data-ttu-id="6055f-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6055f-117">PARAMETERS</span></span>

### <span data-ttu-id="6055f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6055f-118">-DefaultProfile</span></span>
<span data-ttu-id="6055f-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6055f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6055f-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="6055f-120">-MapName</span></span>
<span data-ttu-id="6055f-121">Tümleştirme hesabı eşlemesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6055f-121">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="6055f-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="6055f-122">-Name</span></span>
<span data-ttu-id="6055f-123">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6055f-123">Specifies the name for the integration account.</span></span>

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

### <span data-ttu-id="6055f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6055f-124">-ResourceGroupName</span></span>
<span data-ttu-id="6055f-125">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6055f-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6055f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6055f-126">CommonParameters</span></span>
<span data-ttu-id="6055f-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6055f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6055f-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6055f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6055f-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6055f-129">INPUTS</span></span>

### <span data-ttu-id="6055f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6055f-130">System.String</span></span>

## <span data-ttu-id="6055f-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6055f-131">OUTPUTS</span></span>

### <span data-ttu-id="6055f-132">Microsoft. Azure. Management. Logic. modeller. ıntegrationaccountmap</span><span class="sxs-lookup"><span data-stu-id="6055f-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="6055f-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6055f-133">NOTES</span></span>

## <span data-ttu-id="6055f-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6055f-134">RELATED LINKS</span></span>

[<span data-ttu-id="6055f-135">Yeni-Azıntegrationaccountmap</span><span class="sxs-lookup"><span data-stu-id="6055f-135">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="6055f-136">Remove-Azıntegrationaccountmap</span><span class="sxs-lookup"><span data-stu-id="6055f-136">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="6055f-137">Set-Azıntegrationaccountmap</span><span class="sxs-lookup"><span data-stu-id="6055f-137">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


