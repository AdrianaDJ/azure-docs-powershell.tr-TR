---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5F1A4FE0-CB57-45D3-9F08-879469A61E1E
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccount.md
ms.openlocfilehash: a3a3fc16b253235da82626ab6d827d074f05860d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108206"
---
# <span data-ttu-id="de08c-101">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="de08c-101">New-AzIntegrationAccount</span></span>

## <span data-ttu-id="de08c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de08c-102">SYNOPSIS</span></span>
<span data-ttu-id="de08c-103">Tümleştirme hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="de08c-103">Creates an integration account.</span></span>

## <span data-ttu-id="de08c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="de08c-104">SYNTAX</span></span>

```
New-AzIntegrationAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de08c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="de08c-105">DESCRIPTION</span></span>
<span data-ttu-id="de08c-106">**New-Azıntegrationaccount** cmdlet 'i bir tümleştirme hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="de08c-106">The **New-AzIntegrationAccount** cmdlet creates an integration account.</span></span>
<span data-ttu-id="de08c-107">Bu cmdlet, tümleştirme hesabını temsil eden bir nesne döndürür. Bir ad, konum, kaynak grubu adı ve SKU adı belirtin.</span><span class="sxs-lookup"><span data-stu-id="de08c-107">This cmdlet returns an object that represents the integration account.Specify a name, location, resource group name, and SKU name.</span></span>
<span data-ttu-id="de08c-108">Komut satırında belirttiğiniz şablon parametre dosyası değerleri, bir şablon parametre nesnesindeki şablon parametre değerlerinden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="de08c-108">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="de08c-109">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="de08c-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="de08c-110">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="de08c-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="de08c-111">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="de08c-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="de08c-112">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="de08c-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="de08c-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="de08c-113">EXAMPLES</span></span>

### <span data-ttu-id="de08c-114">Örnek 1: Tümleştirme hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="de08c-114">Example 1: Create an integration account</span></span>
```
PS C:\>New-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Location "brazilsouth" -Sku "Standard"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="de08c-115">Bu komut, belirtilen kaynak grubunda IntegrationAccount31 adlı bir tümleştirme hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="de08c-115">This command creates an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="de08c-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="de08c-116">PARAMETERS</span></span>

### <span data-ttu-id="de08c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de08c-117">-DefaultProfile</span></span>
<span data-ttu-id="de08c-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="de08c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de08c-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="de08c-119">-Location</span></span>
<span data-ttu-id="de08c-120">Tümleştirme hesabı için bir konum belirtir.</span><span class="sxs-lookup"><span data-stu-id="de08c-120">Specifies a location for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de08c-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="de08c-121">-Name</span></span>
<span data-ttu-id="de08c-122">Tümleştirme hesabı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="de08c-122">Specifies a name for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de08c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de08c-123">-ResourceGroupName</span></span>
<span data-ttu-id="de08c-124">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="de08c-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de08c-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="de08c-125">-Sku</span></span>
<span data-ttu-id="de08c-126">Tümleştirme hesabı için bir SKU adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="de08c-126">Specifies a SKU name for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de08c-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="de08c-127">-Confirm</span></span>
<span data-ttu-id="de08c-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="de08c-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de08c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de08c-129">-WhatIf</span></span>
<span data-ttu-id="de08c-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="de08c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de08c-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="de08c-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de08c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de08c-132">CommonParameters</span></span>
<span data-ttu-id="de08c-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="de08c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de08c-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de08c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de08c-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="de08c-135">INPUTS</span></span>

### <span data-ttu-id="de08c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="de08c-136">System.String</span></span>

## <span data-ttu-id="de08c-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="de08c-137">OUTPUTS</span></span>

### <span data-ttu-id="de08c-138">Microsoft. Azure. Management. Logic. modeller. ıntegrationhesabı</span><span class="sxs-lookup"><span data-stu-id="de08c-138">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="de08c-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="de08c-139">NOTES</span></span>

## <span data-ttu-id="de08c-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="de08c-140">RELATED LINKS</span></span>

[<span data-ttu-id="de08c-141">Get-Azıntegrationaccount</span><span class="sxs-lookup"><span data-stu-id="de08c-141">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)

[<span data-ttu-id="de08c-142">Remove-Azıntegrationaccount</span><span class="sxs-lookup"><span data-stu-id="de08c-142">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

[<span data-ttu-id="de08c-143">Set-Azıntegrationaccount</span><span class="sxs-lookup"><span data-stu-id="de08c-143">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)


