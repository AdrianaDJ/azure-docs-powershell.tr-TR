---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 6C16B04B-459A-4B2C-B7DF-AC4D16FF7281
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: 8ad8714a59ac9f0beb0c070d5f9f89c4fbd20a43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592475"
---
# <span data-ttu-id="0275f-101">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="0275f-101">Get-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="0275f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0275f-102">SYNOPSIS</span></span>
<span data-ttu-id="0275f-103">Tümleştirme hesabı şemalarını alır.</span><span class="sxs-lookup"><span data-stu-id="0275f-103">Gets integration account schemas.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0275f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0275f-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountSchema [-ResourceGroupName <String>] [-Name <String>] [-SchemaName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0275f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0275f-105">DESCRIPTION</span></span>
<span data-ttu-id="0275f-106">**Get-AzureRmIntegrationAccountSchema** cmdlet 'i tümleştirme hesabı şemalarını alır.</span><span class="sxs-lookup"><span data-stu-id="0275f-106">The **Get-AzureRmIntegrationAccountSchema** cmdlet gets integration account schemas.</span></span>
<span data-ttu-id="0275f-107">Tümleştirme hesap adını, kaynak grubu adını ve şema adını belirtme.</span><span class="sxs-lookup"><span data-stu-id="0275f-107">Specifying the integration account name, resource group name, and schema name.</span></span>

<span data-ttu-id="0275f-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="0275f-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="0275f-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="0275f-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="0275f-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="0275f-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0275f-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="0275f-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0275f-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0275f-112">EXAMPLES</span></span>

### <span data-ttu-id="0275f-113">Örnek 1: Tümleştirme hesabı şeması alma</span><span class="sxs-lookup"><span data-stu-id="0275f-113">Example 1: Get an integration account schema</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name                 : IntegrationAccountSchema43
Type                 : Microsoft.Logic/integrationAccounts/schemas
CreatedTime          : 3/25/2016 5:42:58 PM
ChangedTime          : 3/25/2016 5:42:58 PM
SchemaType           : Xml
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts469af4f3cf4047b7ac3a08c87948ec5f/3839E_XML_INTEGRATIONACCOUNTSCHEMA43-5A86631F61F
                       14513AA1185A52C6B2874?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 7901
MetaData             :
```

<span data-ttu-id="0275f-114">Bu komut, IntegrationAccountSchema43 adlı tümleştirme hesabı şemasını alır.</span><span class="sxs-lookup"><span data-stu-id="0275f-114">This command gets the integration account schema named IntegrationAccountSchema43.</span></span>

### <span data-ttu-id="0275f-115">Örnek 2: kaynak grubu için tümleştirme hesabı şemalarını alma</span><span class="sxs-lookup"><span data-stu-id="0275f-115">Example 2: Get integration account schemas for a resource group</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name                 : IntegrationAccountSchema43
Type                 : Microsoft.Logic/integrationAccounts/schemas
CreatedTime          : 3/25/2016 5:42:58 PM
ChangedTime          : 3/25/2016 5:42:58 PM
SchemaType           : Xml
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts469af4f3cf4047b7ac3a08c87948ec5f/3839E_XML_INTEGRATIONACCOUNTSCHEMA43-5A86631F61F
                       14513AA1185A52C6B2874?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 7901
MetaData             :
```

<span data-ttu-id="0275f-116">Bu komut, ResourceGroup11 adlı kaynak grubunun tümleştirme hesabı şemalarını alır.</span><span class="sxs-lookup"><span data-stu-id="0275f-116">This command gets the integration account schemas for the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="0275f-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0275f-117">PARAMETERS</span></span>

### <span data-ttu-id="0275f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0275f-118">-DefaultProfile</span></span>
<span data-ttu-id="0275f-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0275f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0275f-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="0275f-120">-Name</span></span>
<span data-ttu-id="0275f-121">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0275f-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="0275f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0275f-122">-ResourceGroupName</span></span>
<span data-ttu-id="0275f-123">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0275f-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0275f-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="0275f-124">-SchemaName</span></span>
<span data-ttu-id="0275f-125">Tümleştirme hesabı şemasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0275f-125">Specifies the name of an integration account schema.</span></span>
<span data-ttu-id="0275f-126">Şemanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0275f-126">Specifies the name of a schema.</span></span>
<span data-ttu-id="0275f-127">.</span><span class="sxs-lookup"><span data-stu-id="0275f-127">.</span></span>

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

### <span data-ttu-id="0275f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0275f-128">CommonParameters</span></span>
<span data-ttu-id="0275f-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0275f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0275f-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0275f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0275f-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0275f-131">INPUTS</span></span>

### <span data-ttu-id="0275f-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0275f-132">None</span></span>
<span data-ttu-id="0275f-133">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="0275f-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0275f-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0275f-134">OUTPUTS</span></span>

### <span data-ttu-id="0275f-135">Microsoft. Azure. Management. Logic. modeller. ıntegrationaccountschema</span><span class="sxs-lookup"><span data-stu-id="0275f-135">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="0275f-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0275f-136">NOTES</span></span>

## <span data-ttu-id="0275f-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0275f-137">RELATED LINKS</span></span>

[<span data-ttu-id="0275f-138">Yeni-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="0275f-138">New-AzureRmIntegrationAccountSchema</span></span>](./New-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="0275f-139">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="0275f-139">Remove-AzureRmIntegrationAccountSchema</span></span>](./Remove-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="0275f-140">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="0275f-140">Set-AzureRmIntegrationAccountSchema</span></span>](./Set-AzureRmIntegrationAccountSchema.md)


