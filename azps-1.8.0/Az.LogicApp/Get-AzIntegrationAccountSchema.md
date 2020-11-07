---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6C16B04B-459A-4B2C-B7DF-AC4D16FF7281
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountSchema.md
ms.openlocfilehash: 9c60e9171385c915785c87d5de217b76a37a4862
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916079"
---
# <span data-ttu-id="16540-101">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="16540-101">Get-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="16540-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16540-102">SYNOPSIS</span></span>
<span data-ttu-id="16540-103">Tümleştirme hesabı şemalarını alır.</span><span class="sxs-lookup"><span data-stu-id="16540-103">Gets integration account schemas.</span></span>

## <span data-ttu-id="16540-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="16540-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountSchema [-ResourceGroupName <String>] [-Name <String>] [-SchemaName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16540-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="16540-105">DESCRIPTION</span></span>
<span data-ttu-id="16540-106">**Get-Azıntegrationaccountschema** cmdlet 'i tümleştirme hesabı şemalarını alır.</span><span class="sxs-lookup"><span data-stu-id="16540-106">The **Get-AzIntegrationAccountSchema** cmdlet gets integration account schemas.</span></span>
<span data-ttu-id="16540-107">Tümleştirme hesap adını, kaynak grubu adını ve şema adını belirtme.</span><span class="sxs-lookup"><span data-stu-id="16540-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="16540-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="16540-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="16540-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="16540-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="16540-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="16540-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="16540-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="16540-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="16540-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="16540-112">EXAMPLES</span></span>

### <span data-ttu-id="16540-113">Örnek 1: Tümleştirme hesabı şeması alma</span><span class="sxs-lookup"><span data-stu-id="16540-113">Example 1: Get an integration account schema</span></span>
```
PS C:\>Get-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
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

<span data-ttu-id="16540-114">Bu komut, IntegrationAccountSchema43 adlı tümleştirme hesabı şemasını alır.</span><span class="sxs-lookup"><span data-stu-id="16540-114">This command gets the integration account schema named IntegrationAccountSchema43.</span></span>

### <span data-ttu-id="16540-115">Örnek 2: kaynak grubu için tümleştirme hesabı şemalarını alma</span><span class="sxs-lookup"><span data-stu-id="16540-115">Example 2: Get integration account schemas for a resource group</span></span>
```
PS C:\>Get-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
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

<span data-ttu-id="16540-116">Bu komut, ResourceGroup11 adlı kaynak grubunun tümleştirme hesabı şemalarını alır.</span><span class="sxs-lookup"><span data-stu-id="16540-116">This command gets the integration account schemas for the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="16540-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="16540-117">PARAMETERS</span></span>

### <span data-ttu-id="16540-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16540-118">-DefaultProfile</span></span>
<span data-ttu-id="16540-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="16540-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16540-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="16540-120">-Name</span></span>
<span data-ttu-id="16540-121">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16540-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="16540-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16540-122">-ResourceGroupName</span></span>
<span data-ttu-id="16540-123">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16540-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="16540-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="16540-124">-SchemaName</span></span>
<span data-ttu-id="16540-125">Tümleştirme hesabı şemasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16540-125">Specifies the name of an integration account schema.</span></span>
<span data-ttu-id="16540-126">Şemanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16540-126">Specifies the name of a schema.</span></span>
<span data-ttu-id="16540-127">.</span><span class="sxs-lookup"><span data-stu-id="16540-127">.</span></span>

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

### <span data-ttu-id="16540-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16540-128">CommonParameters</span></span>
<span data-ttu-id="16540-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="16540-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16540-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16540-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16540-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="16540-131">INPUTS</span></span>

### <span data-ttu-id="16540-132">System. String</span><span class="sxs-lookup"><span data-stu-id="16540-132">System.String</span></span>

## <span data-ttu-id="16540-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="16540-133">OUTPUTS</span></span>

### <span data-ttu-id="16540-134">Microsoft. Azure. Management. Logic. modeller. ıntegrationaccountschema</span><span class="sxs-lookup"><span data-stu-id="16540-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="16540-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="16540-135">NOTES</span></span>

## <span data-ttu-id="16540-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="16540-136">RELATED LINKS</span></span>

[<span data-ttu-id="16540-137">Yeni-Azıntegrationaccountschema</span><span class="sxs-lookup"><span data-stu-id="16540-137">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="16540-138">Remove-Azıntegrationaccountschema</span><span class="sxs-lookup"><span data-stu-id="16540-138">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)

[<span data-ttu-id="16540-139">Set-Azıntegrationaccountschema</span><span class="sxs-lookup"><span data-stu-id="16540-139">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)

