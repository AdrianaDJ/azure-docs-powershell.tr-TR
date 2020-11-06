---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 5F1A4FE0-CB57-45D3-9F08-879469A61E1E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccount.md
ms.openlocfilehash: ec1e223359c3d83a3cfb77810e0e680f7142bc60
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593103"
---
# <span data-ttu-id="75d33-101">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="75d33-101">New-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="75d33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75d33-102">SYNOPSIS</span></span>
<span data-ttu-id="75d33-103">Tümleştirme hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="75d33-103">Creates an integration account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75d33-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="75d33-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75d33-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="75d33-105">DESCRIPTION</span></span>
<span data-ttu-id="75d33-106">**Yeni-AzureRmIntegrationAccount** cmdlet 'i bir tümleştirme hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="75d33-106">The **New-AzureRmIntegrationAccount** cmdlet creates an integration account.</span></span>
<span data-ttu-id="75d33-107">Bu cmdlet, tümleştirme hesabını temsil eden bir nesne döndürür. Bir ad, konum, kaynak grubu adı ve SKU adı belirtin.</span><span class="sxs-lookup"><span data-stu-id="75d33-107">This cmdlet returns an object that represents the integration account.Specify a name, location, resource group name, and SKU name.</span></span>

<span data-ttu-id="75d33-108">Komut satırında belirttiğiniz şablon parametre dosyası değerleri, bir şablon parametre nesnesindeki şablon parametre değerlerinden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="75d33-108">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="75d33-109">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="75d33-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="75d33-110">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="75d33-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="75d33-111">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="75d33-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="75d33-112">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="75d33-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="75d33-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="75d33-113">EXAMPLES</span></span>

### <span data-ttu-id="75d33-114">Örnek 1: Tümleştirme hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="75d33-114">Example 1: Create an integration account</span></span>
```
PS C:\>New-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Location "brazilsouth" -Sku "Standard"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="75d33-115">Bu komut, belirtilen kaynak grubunda IntegrationAccount31 adlı bir tümleştirme hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="75d33-115">This command creates an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="75d33-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="75d33-116">PARAMETERS</span></span>

### <span data-ttu-id="75d33-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="75d33-117">-Location</span></span>
<span data-ttu-id="75d33-118">Tümleştirme hesabı için bir konum belirtir.</span><span class="sxs-lookup"><span data-stu-id="75d33-118">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="75d33-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="75d33-119">-Name</span></span>
<span data-ttu-id="75d33-120">Tümleştirme hesabı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="75d33-120">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="75d33-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75d33-121">-ResourceGroupName</span></span>
<span data-ttu-id="75d33-122">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="75d33-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="75d33-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="75d33-123">-Sku</span></span>
<span data-ttu-id="75d33-124">Tümleştirme hesabı için bir SKU adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="75d33-124">Specifies a SKU name for the integration account.</span></span>

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

### <span data-ttu-id="75d33-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="75d33-125">-Confirm</span></span>
<span data-ttu-id="75d33-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="75d33-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75d33-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75d33-127">-WhatIf</span></span>
<span data-ttu-id="75d33-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="75d33-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75d33-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="75d33-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75d33-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75d33-130">-DefaultProfile</span></span>
<span data-ttu-id="75d33-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="75d33-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75d33-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75d33-132">CommonParameters</span></span>
<span data-ttu-id="75d33-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="75d33-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75d33-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75d33-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75d33-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="75d33-135">INPUTS</span></span>

## <span data-ttu-id="75d33-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="75d33-136">OUTPUTS</span></span>

### <span data-ttu-id="75d33-137">Microsoft. Azure. Management. Logic. modeller. ıntegrationhesabı</span><span class="sxs-lookup"><span data-stu-id="75d33-137">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="75d33-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="75d33-138">NOTES</span></span>

## <span data-ttu-id="75d33-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="75d33-139">RELATED LINKS</span></span>

[<span data-ttu-id="75d33-140">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="75d33-140">Get-AzureRmIntegrationAccount</span></span>](./Get-AzureRmIntegrationAccount.md)

[<span data-ttu-id="75d33-141">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="75d33-141">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)

[<span data-ttu-id="75d33-142">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="75d33-142">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)


