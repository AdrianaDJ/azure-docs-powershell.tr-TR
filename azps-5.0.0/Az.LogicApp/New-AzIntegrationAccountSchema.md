---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 91FFBEE9-A488-49ED-8C6C-2DE891CE0749
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountSchema.md
ms.openlocfilehash: 8887cdf7da3b69d826bedd4f6de97a8cf39d4a6e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280144"
---
# <span data-ttu-id="94289-101">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="94289-101">New-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="94289-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94289-102">SYNOPSIS</span></span>
<span data-ttu-id="94289-103">Tümleştirme hesabı şeması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="94289-103">Creates an integration account schema.</span></span>

## <span data-ttu-id="94289-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="94289-104">SYNTAX</span></span>

```
New-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94289-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="94289-105">DESCRIPTION</span></span>
<span data-ttu-id="94289-106">**New-Azıntegrationaccountschema** cmdlet 'i bir tümleştirme hesabı şeması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="94289-106">The **New-AzIntegrationAccountSchema** cmdlet creates an integration account schema.</span></span>
<span data-ttu-id="94289-107">Bu cmdlet, tümleştirme hesabı şemasını temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="94289-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="94289-108">Tümleştirme hesap adını, kaynak grubu adını, şema adını ve şema tanımını belirtin.</span><span class="sxs-lookup"><span data-stu-id="94289-108">Specify the integration account name, resource group name, schema name, and schema definition.</span></span>
<span data-ttu-id="94289-109">Komut satırında belirttiğiniz şablon parametre dosyası değerleri, bir şablon parametre nesnesindeki şablon parametre değerlerinden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="94289-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="94289-110">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="94289-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="94289-111">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="94289-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="94289-112">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="94289-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="94289-113">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="94289-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="94289-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="94289-114">EXAMPLES</span></span>

### <span data-ttu-id="94289-115">Örnek 1: Tümleştirme hesabı şemasını oluşturma</span><span class="sxs-lookup"><span data-stu-id="94289-115">Example 1: Create the integration account schema</span></span>
```
PS C:\>New-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema1" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema1
Name        : IntegrationAccountSchema1
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="94289-116">Bu komut, belirtilen kaynak grubunda IntegrationAccountSchema1 adlı tümleştirme hesabı şemasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="94289-116">This command creates the integration account schema named IntegrationAccountSchema1 in the specified resource group.</span></span>

## <span data-ttu-id="94289-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="94289-117">PARAMETERS</span></span>

### <span data-ttu-id="94289-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="94289-118">-ContentType</span></span>
<span data-ttu-id="94289-119">Tümleştirme hesabı şemasının içerik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="94289-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="94289-120">Bu cmdlet, harita içerik türü olarak Application/XML destekler.</span><span class="sxs-lookup"><span data-stu-id="94289-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="94289-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94289-121">-DefaultProfile</span></span>
<span data-ttu-id="94289-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="94289-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94289-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="94289-123">-Metadata</span></span>
<span data-ttu-id="94289-124">Şema için bir meta veri nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="94289-124">Specifies a metadata object for the schema.</span></span>

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

### <span data-ttu-id="94289-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="94289-125">-Name</span></span>
<span data-ttu-id="94289-126">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="94289-126">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="94289-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94289-127">-ResourceGroupName</span></span>
<span data-ttu-id="94289-128">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="94289-128">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="94289-129">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="94289-129">-SchemaDefinition</span></span>
<span data-ttu-id="94289-130">Tümleştirme hesabı şeması için bir tanım nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="94289-130">Specifies a definition object for integration account schema.</span></span>
<span data-ttu-id="94289-131">Bu parametreyi veya *Schemafilepath* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="94289-131">Specify either this parameter or the *SchemaFilePath* parameter.</span></span>

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

### <span data-ttu-id="94289-132">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="94289-132">-SchemaFilePath</span></span>
<span data-ttu-id="94289-133">Tümleştirme hesabı şemasının bir tanımının dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="94289-133">Specifies the file path of a definition for the integration account schema.</span></span>
<span data-ttu-id="94289-134">Bu parametreyi veya *Schemadefinition* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="94289-134">Specify either this parameter or the *SchemaDefinition* parameter.</span></span>

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

### <span data-ttu-id="94289-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="94289-135">-SchemaName</span></span>
<span data-ttu-id="94289-136">Tümleştirme hesabı şemasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="94289-136">Specifies a name for the integration account schema.</span></span>

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

### <span data-ttu-id="94289-137">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="94289-137">-SchemaType</span></span>
<span data-ttu-id="94289-138">Tümleştirme hesabı şemasının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="94289-138">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="94289-139">Bu parametre, tür olarak XML 'i destekler.</span><span class="sxs-lookup"><span data-stu-id="94289-139">This parameter supports Xml as the type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xml

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94289-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="94289-140">-Confirm</span></span>
<span data-ttu-id="94289-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="94289-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94289-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94289-142">-WhatIf</span></span>
<span data-ttu-id="94289-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="94289-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94289-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="94289-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94289-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94289-145">CommonParameters</span></span>
<span data-ttu-id="94289-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="94289-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94289-147">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94289-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94289-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="94289-148">INPUTS</span></span>

### <span data-ttu-id="94289-149">System. String</span><span class="sxs-lookup"><span data-stu-id="94289-149">System.String</span></span>

## <span data-ttu-id="94289-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="94289-150">OUTPUTS</span></span>

### <span data-ttu-id="94289-151">Microsoft. Azure. Management. Logic. modeller. ıntegrationaccountschema</span><span class="sxs-lookup"><span data-stu-id="94289-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="94289-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="94289-152">NOTES</span></span>

## <span data-ttu-id="94289-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="94289-153">RELATED LINKS</span></span>

[<span data-ttu-id="94289-154">Get-Azıntegrationaccountschema</span><span class="sxs-lookup"><span data-stu-id="94289-154">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="94289-155">Remove-Azıntegrationaccountschema</span><span class="sxs-lookup"><span data-stu-id="94289-155">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)

[<span data-ttu-id="94289-156">Set-Azıntegrationaccountschema</span><span class="sxs-lookup"><span data-stu-id="94289-156">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


