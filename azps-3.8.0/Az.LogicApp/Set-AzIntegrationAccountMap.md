---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7EF87BE5-FB10-4E5D-A12F-7F50EE6DAD57
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
ms.openlocfilehash: 774fab39542c97dfdd34dbbad672c1dd6b1debc6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095910"
---
# <span data-ttu-id="cd9e5-101">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="cd9e5-101">Set-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="cd9e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd9e5-102">SYNOPSIS</span></span>
<span data-ttu-id="cd9e5-103">Tümleştirme hesabı haritasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="cd9e5-103">Modifies an integration account map.</span></span>

## <span data-ttu-id="cd9e5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cd9e5-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cd9e5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd9e5-105">DESCRIPTION</span></span>
<span data-ttu-id="cd9e5-106">**Set-Azıntegrationaccountmap** cmdlet 'i bir tümleştirme hesabı eşlemini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="cd9e5-106">The **Set-AzIntegrationAccountMap** cmdlet modifies an integration account map.</span></span>
<span data-ttu-id="cd9e5-107">Bu cmdlet Integration Account eşlemesini temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="cd9e5-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="cd9e5-108">Tümleştirme hesap adını, kaynak grubu adını ve harita adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="cd9e5-108">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="cd9e5-109">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="cd9e5-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="cd9e5-110">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="cd9e5-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="cd9e5-111">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="cd9e5-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="cd9e5-112">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="cd9e5-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="cd9e5-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cd9e5-113">EXAMPLES</span></span>

### <span data-ttu-id="cd9e5-114">Örnek 1: Tümleştirme hesabı haritasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="cd9e5-114">Example 1: Modify an integration account map</span></span>
```
PS C:\>Set-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
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

<span data-ttu-id="cd9e5-115">Bu komut, belirtilen kaynak grubundaki tümleştirme hesabı haritasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="cd9e5-115">This command modifies the integration account map in the specified resource group.</span></span>
<span data-ttu-id="cd9e5-116">Komut, $MapContent değişkeninde depolanan bir harita tanımını önceki komutla belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd9e5-116">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

## <span data-ttu-id="cd9e5-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cd9e5-117">PARAMETERS</span></span>

### <span data-ttu-id="cd9e5-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="cd9e5-118">-ContentType</span></span>
<span data-ttu-id="cd9e5-119">Tümleştirme hesabı haritası için içerik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd9e5-119">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="cd9e5-120">Bu cmdlet, harita içerik türü olarak Application/XML destekler.</span><span class="sxs-lookup"><span data-stu-id="cd9e5-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="cd9e5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd9e5-121">-DefaultProfile</span></span>
<span data-ttu-id="cd9e5-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="cd9e5-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd9e5-123">-Force</span><span class="sxs-lookup"><span data-stu-id="cd9e5-123">-Force</span></span>
<span data-ttu-id="cd9e5-124">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="cd9e5-124">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd9e5-125">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="cd9e5-125">-MapDefinition</span></span>
<span data-ttu-id="cd9e5-126">Tümleştirme hesabı haritası için bir tanım nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd9e5-126">Specifies a definition object for integration account map.</span></span>

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

### <span data-ttu-id="cd9e5-127">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="cd9e5-127">-MapFilePath</span></span>
<span data-ttu-id="cd9e5-128">Tümleştirme hesabı haritası için bir tanımın dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd9e5-128">Specifies the file path of a definition for the integration account map.</span></span>

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

### <span data-ttu-id="cd9e5-129">-MapName</span><span class="sxs-lookup"><span data-stu-id="cd9e5-129">-MapName</span></span>
<span data-ttu-id="cd9e5-130">Tümleştirme hesabı eşlemesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd9e5-130">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="cd9e5-131">-MapType</span><span class="sxs-lookup"><span data-stu-id="cd9e5-131">-MapType</span></span>
<span data-ttu-id="cd9e5-132">Tümleştirme hesabı haritasının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd9e5-132">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="cd9e5-133">Bu cmdlet XSLT 'yi harita türü olarak destekler.</span><span class="sxs-lookup"><span data-stu-id="cd9e5-133">This cmdlet supports Xslt as a map type.</span></span>

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

### <span data-ttu-id="cd9e5-134">-Metadata</span><span class="sxs-lookup"><span data-stu-id="cd9e5-134">-Metadata</span></span>
<span data-ttu-id="cd9e5-135">Harita için meta veri nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd9e5-135">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="cd9e5-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="cd9e5-136">-Name</span></span>
<span data-ttu-id="cd9e5-137">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd9e5-137">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="cd9e5-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd9e5-138">-ResourceGroupName</span></span>
<span data-ttu-id="cd9e5-139">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd9e5-139">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="cd9e5-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="cd9e5-140">-Confirm</span></span>
<span data-ttu-id="cd9e5-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cd9e5-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd9e5-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd9e5-142">-WhatIf</span></span>
<span data-ttu-id="cd9e5-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cd9e5-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd9e5-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cd9e5-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd9e5-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd9e5-145">CommonParameters</span></span>
<span data-ttu-id="cd9e5-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cd9e5-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd9e5-147">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd9e5-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd9e5-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cd9e5-148">INPUTS</span></span>

### <span data-ttu-id="cd9e5-149">System. String</span><span class="sxs-lookup"><span data-stu-id="cd9e5-149">System.String</span></span>

## <span data-ttu-id="cd9e5-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cd9e5-150">OUTPUTS</span></span>

### <span data-ttu-id="cd9e5-151">Microsoft. Azure. Management. Logic. modeller. ıntegrationaccountmap</span><span class="sxs-lookup"><span data-stu-id="cd9e5-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="cd9e5-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cd9e5-152">NOTES</span></span>

## <span data-ttu-id="cd9e5-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cd9e5-153">RELATED LINKS</span></span>

[<span data-ttu-id="cd9e5-154">Get-Azıntegrationaccountmap</span><span class="sxs-lookup"><span data-stu-id="cd9e5-154">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="cd9e5-155">Yeni-Azıntegrationaccountmap</span><span class="sxs-lookup"><span data-stu-id="cd9e5-155">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="cd9e5-156">Remove-Azıntegrationaccountmap</span><span class="sxs-lookup"><span data-stu-id="cd9e5-156">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)


