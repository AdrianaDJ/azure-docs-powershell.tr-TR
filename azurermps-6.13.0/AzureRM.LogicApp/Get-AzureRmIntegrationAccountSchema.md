---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 6C16B04B-459A-4B2C-B7DF-AC4D16FF7281
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: 06aebcf21b7a9fb69887c8922343faf7867d796c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593237"
---
# <span data-ttu-id="7f57a-101">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="7f57a-101">Get-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="7f57a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f57a-102">SYNOPSIS</span></span>
<span data-ttu-id="7f57a-103">Tümleştirme hesabı şemalarını alır.</span><span class="sxs-lookup"><span data-stu-id="7f57a-103">Gets integration account schemas.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f57a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f57a-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountSchema [-ResourceGroupName <String>] [-Name <String>] [-SchemaName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f57a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f57a-105">DESCRIPTION</span></span>
<span data-ttu-id="7f57a-106">**Get-AzureRmIntegrationAccountSchema** cmdlet 'i tümleştirme hesabı şemalarını alır.</span><span class="sxs-lookup"><span data-stu-id="7f57a-106">The **Get-AzureRmIntegrationAccountSchema** cmdlet gets integration account schemas.</span></span>
<span data-ttu-id="7f57a-107">Tümleştirme hesap adını, kaynak grubu adını ve şema adını belirtme.</span><span class="sxs-lookup"><span data-stu-id="7f57a-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="7f57a-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="7f57a-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="7f57a-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="7f57a-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="7f57a-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="7f57a-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="7f57a-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="7f57a-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="7f57a-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f57a-112">EXAMPLES</span></span>

### <span data-ttu-id="7f57a-113">Örnek 1: Tümleştirme hesabı şeması alma</span><span class="sxs-lookup"><span data-stu-id="7f57a-113">Example 1: Get an integration account schema</span></span>
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

<span data-ttu-id="7f57a-114">Bu komut, IntegrationAccountSchema43 adlı tümleştirme hesabı şemasını alır.</span><span class="sxs-lookup"><span data-stu-id="7f57a-114">This command gets the integration account schema named IntegrationAccountSchema43.</span></span>

### <span data-ttu-id="7f57a-115">Örnek 2: kaynak grubu için tümleştirme hesabı şemalarını alma</span><span class="sxs-lookup"><span data-stu-id="7f57a-115">Example 2: Get integration account schemas for a resource group</span></span>
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

<span data-ttu-id="7f57a-116">Bu komut, ResourceGroup11 adlı kaynak grubunun tümleştirme hesabı şemalarını alır.</span><span class="sxs-lookup"><span data-stu-id="7f57a-116">This command gets the integration account schemas for the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="7f57a-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f57a-117">PARAMETERS</span></span>

### <span data-ttu-id="7f57a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f57a-118">-DefaultProfile</span></span>
<span data-ttu-id="7f57a-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7f57a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f57a-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="7f57a-120">-Name</span></span>
<span data-ttu-id="7f57a-121">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f57a-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="7f57a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f57a-122">-ResourceGroupName</span></span>
<span data-ttu-id="7f57a-123">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f57a-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7f57a-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="7f57a-124">-SchemaName</span></span>
<span data-ttu-id="7f57a-125">Tümleştirme hesabı şemasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f57a-125">Specifies the name of an integration account schema.</span></span>
<span data-ttu-id="7f57a-126">Şemanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f57a-126">Specifies the name of a schema.</span></span>
<span data-ttu-id="7f57a-127">.</span><span class="sxs-lookup"><span data-stu-id="7f57a-127">.</span></span>

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

### <span data-ttu-id="7f57a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f57a-128">CommonParameters</span></span>
<span data-ttu-id="7f57a-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7f57a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f57a-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f57a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f57a-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f57a-131">INPUTS</span></span>

### <span data-ttu-id="7f57a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7f57a-132">System.String</span></span>

## <span data-ttu-id="7f57a-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f57a-133">OUTPUTS</span></span>

### <span data-ttu-id="7f57a-134">Microsoft. Azure. Management. Logic. modeller. ıntegrationaccountschema</span><span class="sxs-lookup"><span data-stu-id="7f57a-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="7f57a-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f57a-135">NOTES</span></span>

## <span data-ttu-id="7f57a-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f57a-136">RELATED LINKS</span></span>

[<span data-ttu-id="7f57a-137">Yeni-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="7f57a-137">New-AzureRmIntegrationAccountSchema</span></span>](./New-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="7f57a-138">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="7f57a-138">Remove-AzureRmIntegrationAccountSchema</span></span>](./Remove-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="7f57a-139">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="7f57a-139">Set-AzureRmIntegrationAccountSchema</span></span>](./Set-AzureRmIntegrationAccountSchema.md)


