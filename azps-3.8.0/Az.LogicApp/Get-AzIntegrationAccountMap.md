---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4F65A8B3-A250-41C1-9AA5-DBEB3193C401
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountMap.md
ms.openlocfilehash: 99f6bcda0360395826dedc02e3d8b968ee23795d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937713"
---
# <span data-ttu-id="b3c28-101">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b3c28-101">Get-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="b3c28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3c28-102">SYNOPSIS</span></span>
<span data-ttu-id="b3c28-103">Tümleştirme hesabı haritasını alır.</span><span class="sxs-lookup"><span data-stu-id="b3c28-103">Gets an integration account map.</span></span>

## <span data-ttu-id="b3c28-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3c28-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountMap [-ResourceGroupName <String>] [-Name <String>] [-MapName <String>]
 [-MapType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3c28-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3c28-105">DESCRIPTION</span></span>
<span data-ttu-id="b3c28-106">**Get-Azıntegrationaccountmap** cmdlet 'i bir kaynak grubundan tümleştirme hesabı haritasını alır.</span><span class="sxs-lookup"><span data-stu-id="b3c28-106">The **Get-AzIntegrationAccountMap** cmdlet gets integration account map from a resource group.</span></span>
<span data-ttu-id="b3c28-107">Tümleştirme hesap adını, kaynak grubu adını ve harita adını belirtme.</span><span class="sxs-lookup"><span data-stu-id="b3c28-107">Specifying the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="b3c28-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="b3c28-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b3c28-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="b3c28-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b3c28-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="b3c28-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b3c28-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="b3c28-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b3c28-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3c28-112">EXAMPLES</span></span>

### <span data-ttu-id="b3c28-113">Örnek 1: Tümleştirme hesabı haritasını alma</span><span class="sxs-lookup"><span data-stu-id="b3c28-113">Example 1: Get an integration account map</span></span>
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

<span data-ttu-id="b3c28-114">Bu komut, belirtilen kaynak grubundaki IntegrationAccountMap47 adlı bir tümleştirme hesabı haritasını alır.</span><span class="sxs-lookup"><span data-stu-id="b3c28-114">This command gets an integration account map named IntegrationAccountMap47 in the specified resource group.</span></span>

### <span data-ttu-id="b3c28-115">Örnek 2: Tümleştirme hesabı adlarını tümleştirme hesap adıyla alma</span><span class="sxs-lookup"><span data-stu-id="b3c28-115">Example 2: Get integration account maps by integration account name</span></span>
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

<span data-ttu-id="b3c28-116">Bu komut Integration Account adını Integration Account Name ile alır.</span><span class="sxs-lookup"><span data-stu-id="b3c28-116">This command gets the integration account maps by integration account name.</span></span>

## <span data-ttu-id="b3c28-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3c28-117">PARAMETERS</span></span>

### <span data-ttu-id="b3c28-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3c28-118">-DefaultProfile</span></span>
<span data-ttu-id="b3c28-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b3c28-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3c28-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="b3c28-120">-MapName</span></span>
<span data-ttu-id="b3c28-121">Tümleştirme hesabı eşlemesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3c28-121">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="b3c28-122">-MapType</span><span class="sxs-lookup"><span data-stu-id="b3c28-122">-MapType</span></span>
<span data-ttu-id="b3c28-123">Tümleştirme hesabı harita türü.</span><span class="sxs-lookup"><span data-stu-id="b3c28-123">The integration account map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xslt, Xslt20, Xslt30, Liquid

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3c28-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="b3c28-124">-Name</span></span>
<span data-ttu-id="b3c28-125">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3c28-125">Specifies the name for the integration account.</span></span>

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

### <span data-ttu-id="b3c28-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3c28-126">-ResourceGroupName</span></span>
<span data-ttu-id="b3c28-127">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3c28-127">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b3c28-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3c28-128">CommonParameters</span></span>
<span data-ttu-id="b3c28-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3c28-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3c28-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3c28-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3c28-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3c28-131">INPUTS</span></span>

### <span data-ttu-id="b3c28-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b3c28-132">System.String</span></span>

## <span data-ttu-id="b3c28-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3c28-133">OUTPUTS</span></span>

### <span data-ttu-id="b3c28-134">Microsoft. Azure. Management. Logic. modeller. ıntegrationaccountmap</span><span class="sxs-lookup"><span data-stu-id="b3c28-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="b3c28-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3c28-135">NOTES</span></span>

## <span data-ttu-id="b3c28-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3c28-136">RELATED LINKS</span></span>

[<span data-ttu-id="b3c28-137">Yeni-Azıntegrationaccountmap</span><span class="sxs-lookup"><span data-stu-id="b3c28-137">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="b3c28-138">Remove-Azıntegrationaccountmap</span><span class="sxs-lookup"><span data-stu-id="b3c28-138">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="b3c28-139">Set-Azıntegrationaccountmap</span><span class="sxs-lookup"><span data-stu-id="b3c28-139">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


