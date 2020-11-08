---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: DF71430C-F33F-409B-A550-CC7285252E91
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
ms.openlocfilehash: a7803d95c2991dd829053a6d508432931701a220
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274473"
---
# <span data-ttu-id="79ea5-101">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="79ea5-101">New-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="79ea5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79ea5-102">SYNOPSIS</span></span>
<span data-ttu-id="79ea5-103">Tümleştirme hesabı haritası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="79ea5-103">Creates an integration account map.</span></span>

## <span data-ttu-id="79ea5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="79ea5-104">SYNTAX</span></span>

```
New-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79ea5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="79ea5-105">DESCRIPTION</span></span>
<span data-ttu-id="79ea5-106">**New-Azıntegrationaccountmap** cmdlet 'i bir tümleştirme hesabı haritası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="79ea5-106">The **New-AzIntegrationAccountMap** cmdlet creates an integration account map.</span></span>
<span data-ttu-id="79ea5-107">Bu cmdlet Integration Account eşlemesini temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="79ea5-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="79ea5-108">Tümleştirme hesap adını, kaynak grubu adını, harita adını ve harita tanımını belirtme.</span><span class="sxs-lookup"><span data-stu-id="79ea5-108">Specifying the integration account name, resource group name, map name, and map definition.</span></span>
<span data-ttu-id="79ea5-109">Komut satırında belirttiğiniz şablon parametre dosyası değerleri, bir şablon parametre nesnesindeki şablon parametre değerlerinden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="79ea5-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="79ea5-110">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="79ea5-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="79ea5-111">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="79ea5-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="79ea5-112">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="79ea5-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="79ea5-113">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="79ea5-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="79ea5-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="79ea5-114">EXAMPLES</span></span>

### <span data-ttu-id="79ea5-115">Örnek 1: Tümleştirme hesabı haritası oluşturma</span><span class="sxs-lookup"><span data-stu-id="79ea5-115">Example 1: Create an integration account map</span></span>
```powershell
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

<span data-ttu-id="79ea5-116">Bu komut, belirtilen kaynak grubunda tümleştirme hesabı haritasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="79ea5-116">This command creates the integration account map in the specified resource group.</span></span>
<span data-ttu-id="79ea5-117">Komut, $MapContent değişkeninde depolanan bir harita tanımını önceki komutla belirtir.</span><span class="sxs-lookup"><span data-stu-id="79ea5-117">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

### <span data-ttu-id="79ea5-118">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="79ea5-118">Example 2</span></span>

<span data-ttu-id="79ea5-119">Tümleştirme hesabı haritası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="79ea5-119">Creates an integration account map.</span></span> <span data-ttu-id="79ea5-120">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="79ea5-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzIntegrationAccountMap -MapFilePath <String> -MapName 'IntegrationAccountMap47' -MapType Xslt -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="79ea5-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="79ea5-121">PARAMETERS</span></span>

### <span data-ttu-id="79ea5-122">-ContentType</span><span class="sxs-lookup"><span data-stu-id="79ea5-122">-ContentType</span></span>
<span data-ttu-id="79ea5-123">Tümleştirme hesabı haritası için içerik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="79ea5-123">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="79ea5-124">Bu cmdlet, harita içerik türü olarak Application/XML destekler.</span><span class="sxs-lookup"><span data-stu-id="79ea5-124">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="79ea5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79ea5-125">-DefaultProfile</span></span>
<span data-ttu-id="79ea5-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="79ea5-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79ea5-127">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="79ea5-127">-MapDefinition</span></span>
<span data-ttu-id="79ea5-128">Tümleştirme hesabı haritası için bir tanım nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="79ea5-128">Specifies a definition object for integration account map.</span></span>
<span data-ttu-id="79ea5-129">Bu parametreyi veya *MapFilePath* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="79ea5-129">Specify either this parameter or the *MapFilePath* parameter.</span></span>

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

### <span data-ttu-id="79ea5-130">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="79ea5-130">-MapFilePath</span></span>
<span data-ttu-id="79ea5-131">Tümleştirme hesabı haritası için bir tanımın dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="79ea5-131">Specifies the file path of a definition for the integration account map.</span></span> <span data-ttu-id="79ea5-132">Bu parametreyi veya *Mapdefinition* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="79ea5-132">Specify either this parameter or the *MapDefinition* parameter.</span></span>

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

### <span data-ttu-id="79ea5-133">-MapName</span><span class="sxs-lookup"><span data-stu-id="79ea5-133">-MapName</span></span>
<span data-ttu-id="79ea5-134">Tümleştirme hesabı haritası için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="79ea5-134">Specifies a name for the integration account map.</span></span>

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

### <span data-ttu-id="79ea5-135">-MapType</span><span class="sxs-lookup"><span data-stu-id="79ea5-135">-MapType</span></span>
<span data-ttu-id="79ea5-136">Tümleştirme hesabı haritasının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="79ea5-136">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="79ea5-137">Bu cmdlet XSLT 'yi harita türü olarak destekler.</span><span class="sxs-lookup"><span data-stu-id="79ea5-137">This cmdlet supports Xslt as a map type.</span></span>

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

### <span data-ttu-id="79ea5-138">-Metadata</span><span class="sxs-lookup"><span data-stu-id="79ea5-138">-Metadata</span></span>
<span data-ttu-id="79ea5-139">Harita için meta veri nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="79ea5-139">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="79ea5-140">-Ad</span><span class="sxs-lookup"><span data-stu-id="79ea5-140">-Name</span></span>
<span data-ttu-id="79ea5-141">Tümleştirme hesabı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="79ea5-141">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="79ea5-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79ea5-142">-ResourceGroupName</span></span>
<span data-ttu-id="79ea5-143">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79ea5-143">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="79ea5-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="79ea5-144">-Confirm</span></span>
<span data-ttu-id="79ea5-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="79ea5-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79ea5-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79ea5-146">-WhatIf</span></span>
<span data-ttu-id="79ea5-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="79ea5-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79ea5-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="79ea5-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79ea5-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79ea5-149">CommonParameters</span></span>
<span data-ttu-id="79ea5-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="79ea5-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79ea5-151">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79ea5-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79ea5-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="79ea5-152">INPUTS</span></span>

### <span data-ttu-id="79ea5-153">System. String</span><span class="sxs-lookup"><span data-stu-id="79ea5-153">System.String</span></span>

## <span data-ttu-id="79ea5-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="79ea5-154">OUTPUTS</span></span>

### <span data-ttu-id="79ea5-155">Microsoft. Azure. Management. Logic. modeller. ıntegrationaccountmap</span><span class="sxs-lookup"><span data-stu-id="79ea5-155">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="79ea5-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="79ea5-156">NOTES</span></span>

## <span data-ttu-id="79ea5-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="79ea5-157">RELATED LINKS</span></span>

[<span data-ttu-id="79ea5-158">Get-Azıntegrationaccountmap</span><span class="sxs-lookup"><span data-stu-id="79ea5-158">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="79ea5-159">Remove-Azıntegrationaccountmap</span><span class="sxs-lookup"><span data-stu-id="79ea5-159">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="79ea5-160">Set-Azıntegrationaccountmap</span><span class="sxs-lookup"><span data-stu-id="79ea5-160">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


