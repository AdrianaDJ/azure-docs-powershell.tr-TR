---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: DF71430C-F33F-409B-A550-CC7285252E91
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
ms.openlocfilehash: e483d2f88f12655283c94d8c42e9926e4dd6cddb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751528"
---
# <span data-ttu-id="ae072-101">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="ae072-101">New-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="ae072-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae072-102">SYNOPSIS</span></span>
<span data-ttu-id="ae072-103">Tümleştirme hesabı haritası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ae072-103">Creates an integration account map.</span></span>

## <span data-ttu-id="ae072-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ae072-104">SYNTAX</span></span>

```
New-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae072-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ae072-105">DESCRIPTION</span></span>
<span data-ttu-id="ae072-106">**New-Azıntegrationaccountmap** cmdlet 'i bir tümleştirme hesabı haritası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ae072-106">The **New-AzIntegrationAccountMap** cmdlet creates an integration account map.</span></span>
<span data-ttu-id="ae072-107">Bu cmdlet Integration Account eşlemesini temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="ae072-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="ae072-108">Tümleştirme hesap adını, kaynak grubu adını, harita adını ve harita tanımını belirtme.</span><span class="sxs-lookup"><span data-stu-id="ae072-108">Specifying the integration account name, resource group name, map name, and map definition.</span></span>
<span data-ttu-id="ae072-109">Komut satırında belirttiğiniz şablon parametre dosyası değerleri, bir şablon parametre nesnesindeki şablon parametre değerlerinden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="ae072-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="ae072-110">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="ae072-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ae072-111">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="ae072-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ae072-112">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="ae072-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ae072-113">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="ae072-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ae072-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ae072-114">EXAMPLES</span></span>

### <span data-ttu-id="ae072-115">Örnek 1: Tümleştirme hesabı haritası oluşturma</span><span class="sxs-lookup"><span data-stu-id="ae072-115">Example 1: Create an integration account map</span></span>
```
PS C:\>New-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
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

<span data-ttu-id="ae072-116">Bu komut, belirtilen kaynak grubunda tümleştirme hesabı haritasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ae072-116">This command creates the integration account map in the specified resource group.</span></span>
<span data-ttu-id="ae072-117">Komut, $MapContent değişkeninde depolanan bir harita tanımını önceki komutla belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae072-117">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

## <span data-ttu-id="ae072-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ae072-118">PARAMETERS</span></span>

### <span data-ttu-id="ae072-119">-ContentType</span><span class="sxs-lookup"><span data-stu-id="ae072-119">-ContentType</span></span>
<span data-ttu-id="ae072-120">Tümleştirme hesabı haritası için içerik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae072-120">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="ae072-121">Bu cmdlet, harita içerik türü olarak Application/XML destekler.</span><span class="sxs-lookup"><span data-stu-id="ae072-121">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="ae072-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae072-122">-DefaultProfile</span></span>
<span data-ttu-id="ae072-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ae072-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae072-124">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="ae072-124">-MapDefinition</span></span>
<span data-ttu-id="ae072-125">Tümleştirme hesabı haritası için bir tanım nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae072-125">Specifies a definition object for integration account map.</span></span>
<span data-ttu-id="ae072-126">Bu parametreyi veya *MapFilePath* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="ae072-126">Specify either this parameter or the *MapFilePath* parameter.</span></span>

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

### <span data-ttu-id="ae072-127">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="ae072-127">-MapFilePath</span></span>
<span data-ttu-id="ae072-128">Tümleştirme hesabı haritası için bir tanımın dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae072-128">Specifies the file path of a definition for the integration account map.</span></span> <span data-ttu-id="ae072-129">Bu parametreyi veya *Mapdefinition* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="ae072-129">Specify either this parameter or the *MapDefinition* parameter.</span></span>

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

### <span data-ttu-id="ae072-130">-MapName</span><span class="sxs-lookup"><span data-stu-id="ae072-130">-MapName</span></span>
<span data-ttu-id="ae072-131">Tümleştirme hesabı haritası için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae072-131">Specifies a name for the integration account map.</span></span>

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

### <span data-ttu-id="ae072-132">-MapType</span><span class="sxs-lookup"><span data-stu-id="ae072-132">-MapType</span></span>
<span data-ttu-id="ae072-133">Tümleştirme hesabı haritasının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae072-133">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="ae072-134">Bu cmdlet XSLT 'yi harita türü olarak destekler.</span><span class="sxs-lookup"><span data-stu-id="ae072-134">This cmdlet supports Xslt as a map type.</span></span>

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

### <span data-ttu-id="ae072-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="ae072-135">-Metadata</span></span>
<span data-ttu-id="ae072-136">Harita için meta veri nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae072-136">Specifies a metadata object for the map.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae072-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="ae072-137">-Name</span></span>
<span data-ttu-id="ae072-138">Tümleştirme hesabı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae072-138">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="ae072-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae072-139">-ResourceGroupName</span></span>
<span data-ttu-id="ae072-140">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae072-140">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ae072-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="ae072-141">-Confirm</span></span>
<span data-ttu-id="ae072-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ae072-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae072-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae072-143">-WhatIf</span></span>
<span data-ttu-id="ae072-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ae072-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae072-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ae072-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae072-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae072-146">CommonParameters</span></span>
<span data-ttu-id="ae072-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ae072-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae072-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae072-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae072-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ae072-149">INPUTS</span></span>

### <span data-ttu-id="ae072-150">System. String</span><span class="sxs-lookup"><span data-stu-id="ae072-150">System.String</span></span>

## <span data-ttu-id="ae072-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ae072-151">OUTPUTS</span></span>

### <span data-ttu-id="ae072-152">Microsoft. Azure. Management. Logic. modeller. ıntegrationaccountmap</span><span class="sxs-lookup"><span data-stu-id="ae072-152">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="ae072-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ae072-153">NOTES</span></span>

## <span data-ttu-id="ae072-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ae072-154">RELATED LINKS</span></span>

[<span data-ttu-id="ae072-155">Get-Azıntegrationaccountmap</span><span class="sxs-lookup"><span data-stu-id="ae072-155">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="ae072-156">Remove-Azıntegrationaccountmap</span><span class="sxs-lookup"><span data-stu-id="ae072-156">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="ae072-157">Set-Azıntegrationaccountmap</span><span class="sxs-lookup"><span data-stu-id="ae072-157">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


