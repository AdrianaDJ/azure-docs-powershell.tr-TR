---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: DF71430C-F33F-409B-A550-CC7285252E91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/new-azurermintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: ad92d2c6a2bcf6dbf9a3bcb75970d3db50adbac0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590999"
---
# <span data-ttu-id="dee55-101">New-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="dee55-101">New-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="dee55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dee55-102">SYNOPSIS</span></span>
<span data-ttu-id="dee55-103">Tümleştirme hesabı haritası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dee55-103">Creates an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dee55-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dee55-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dee55-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dee55-105">DESCRIPTION</span></span>
<span data-ttu-id="dee55-106">**Yeni-AzureRmIntegrationAccountMap** cmdlet 'i bir tümleştirme hesabı haritası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dee55-106">The **New-AzureRmIntegrationAccountMap** cmdlet creates an integration account map.</span></span>
<span data-ttu-id="dee55-107">Bu cmdlet Integration Account eşlemesini temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="dee55-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="dee55-108">Tümleştirme hesap adını, kaynak grubu adını, harita adını ve harita tanımını belirtme.</span><span class="sxs-lookup"><span data-stu-id="dee55-108">Specifying the integration account name, resource group name, map name, and map definition.</span></span>

<span data-ttu-id="dee55-109">Komut satırında belirttiğiniz şablon parametre dosyası değerleri, bir şablon parametre nesnesindeki şablon parametre değerlerinden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="dee55-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="dee55-110">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="dee55-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="dee55-111">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="dee55-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="dee55-112">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="dee55-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="dee55-113">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="dee55-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="dee55-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dee55-114">EXAMPLES</span></span>

### <span data-ttu-id="dee55-115">Örnek 1: Tümleştirme hesabı haritası oluşturma</span><span class="sxs-lookup"><span data-stu-id="dee55-115">Example 1: Create an integration account map</span></span>
```
PS C:\>New-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
Id          : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/maps/IntegrationAccountMap47
Name        : IntegrationAccountMap47
Type        : Microsoft.Logic/integrationAccounts/maps
CreatedTime : 3/26/2016 7:12:22 PM
ChangedTime : 3/26/2016 7:12:22 PM
MapType     : Xslt
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/99D1E_XSLT_INTEGRATIONACCOUNTMAP47-9C97D973088B4256A1893B
              BCB1F85246?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 3056
Metadata    :
```

<span data-ttu-id="dee55-116">Bu komut, belirtilen kaynak grubunda tümleştirme hesabı haritasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dee55-116">This command creates the integration account map in the specified resource group.</span></span>
<span data-ttu-id="dee55-117">Komut, $MapContent değişkeninde depolanan bir harita tanımını önceki komutla belirtir.</span><span class="sxs-lookup"><span data-stu-id="dee55-117">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

## <span data-ttu-id="dee55-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dee55-118">PARAMETERS</span></span>

### <span data-ttu-id="dee55-119">-ContentType</span><span class="sxs-lookup"><span data-stu-id="dee55-119">-ContentType</span></span>
<span data-ttu-id="dee55-120">Tümleştirme hesabı haritası için içerik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="dee55-120">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="dee55-121">Bu cmdlet, harita içerik türü olarak Application/XML destekler.</span><span class="sxs-lookup"><span data-stu-id="dee55-121">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="dee55-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dee55-122">-DefaultProfile</span></span>
<span data-ttu-id="dee55-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="dee55-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dee55-124">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="dee55-124">-MapDefinition</span></span>
<span data-ttu-id="dee55-125">Tümleştirme hesabı haritası için bir tanım nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="dee55-125">Specifies a definition object for integration account map.</span></span>
<span data-ttu-id="dee55-126">Bu parametreyi veya *MapFilePath* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="dee55-126">Specify either this parameter or the *MapFilePath* parameter.</span></span>

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

### <span data-ttu-id="dee55-127">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="dee55-127">-MapFilePath</span></span>
<span data-ttu-id="dee55-128">Tümleştirme hesabı haritası için bir tanımın dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="dee55-128">Specifies the file path of a definition for the integration account map.</span></span> <span data-ttu-id="dee55-129">Bu parametreyi veya *Mapdefinition* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="dee55-129">Specify either this parameter or the *MapDefinition* parameter.</span></span>

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

### <span data-ttu-id="dee55-130">-MapName</span><span class="sxs-lookup"><span data-stu-id="dee55-130">-MapName</span></span>
<span data-ttu-id="dee55-131">Tümleştirme hesabı haritası için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="dee55-131">Specifies a name for the integration account map.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dee55-132">-MapType</span><span class="sxs-lookup"><span data-stu-id="dee55-132">-MapType</span></span>
<span data-ttu-id="dee55-133">Tümleştirme hesabı haritasının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="dee55-133">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="dee55-134">Bu cmdlet XSLT 'yi harita türü olarak destekler.</span><span class="sxs-lookup"><span data-stu-id="dee55-134">This cmdlet supports Xslt as a map type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Xslt

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dee55-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="dee55-135">-Metadata</span></span>
<span data-ttu-id="dee55-136">Harita için meta veri nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="dee55-136">Specifies a metadata object for the map.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dee55-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="dee55-137">-Name</span></span>
<span data-ttu-id="dee55-138">Tümleştirme hesabı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="dee55-138">Specifies a name for the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dee55-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dee55-139">-ResourceGroupName</span></span>
<span data-ttu-id="dee55-140">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dee55-140">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dee55-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="dee55-141">-Confirm</span></span>
<span data-ttu-id="dee55-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dee55-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dee55-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dee55-143">-WhatIf</span></span>
<span data-ttu-id="dee55-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dee55-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dee55-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dee55-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dee55-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dee55-146">CommonParameters</span></span>
<span data-ttu-id="dee55-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dee55-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dee55-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dee55-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dee55-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dee55-149">INPUTS</span></span>

### <span data-ttu-id="dee55-150">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="dee55-150">None</span></span>
<span data-ttu-id="dee55-151">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="dee55-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dee55-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dee55-152">OUTPUTS</span></span>

### <span data-ttu-id="dee55-153">Microsoft. Azure. Management. Logic. modeller. ıntegrationaccountmap</span><span class="sxs-lookup"><span data-stu-id="dee55-153">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="dee55-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dee55-154">NOTES</span></span>

## <span data-ttu-id="dee55-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dee55-155">RELATED LINKS</span></span>

[<span data-ttu-id="dee55-156">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="dee55-156">Get-AzureRmIntegrationAccountMap</span></span>](./Get-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="dee55-157">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="dee55-157">Remove-AzureRmIntegrationAccountMap</span></span>](./Remove-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="dee55-158">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="dee55-158">Set-AzureRmIntegrationAccountMap</span></span>](./Set-AzureRmIntegrationAccountMap.md)


