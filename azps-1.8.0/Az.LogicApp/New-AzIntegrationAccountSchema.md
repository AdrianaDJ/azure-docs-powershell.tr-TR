---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 91FFBEE9-A488-49ED-8C6C-2DE891CE0749
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountSchema.md
ms.openlocfilehash: 23dd1ba36a634e1b1d49e4623a9c652cda5bab27
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916019"
---
# <span data-ttu-id="77657-101">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="77657-101">New-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="77657-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77657-102">SYNOPSIS</span></span>
<span data-ttu-id="77657-103">Tümleştirme hesabı şeması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="77657-103">Creates an integration account schema.</span></span>

## <span data-ttu-id="77657-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="77657-104">SYNTAX</span></span>

```
New-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77657-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="77657-105">DESCRIPTION</span></span>
<span data-ttu-id="77657-106">**New-Azıntegrationaccountschema** cmdlet 'i bir tümleştirme hesabı şeması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="77657-106">The **New-AzIntegrationAccountSchema** cmdlet creates an integration account schema.</span></span>
<span data-ttu-id="77657-107">Bu cmdlet, tümleştirme hesabı şemasını temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="77657-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="77657-108">Tümleştirme hesap adını, kaynak grubu adını, şema adını ve şema tanımını belirtin.</span><span class="sxs-lookup"><span data-stu-id="77657-108">Specify the integration account name, resource group name, schema name, and schema definition.</span></span>
<span data-ttu-id="77657-109">Komut satırında belirttiğiniz şablon parametre dosyası değerleri, bir şablon parametre nesnesindeki şablon parametre değerlerinden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="77657-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="77657-110">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="77657-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="77657-111">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="77657-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="77657-112">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="77657-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="77657-113">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="77657-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="77657-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="77657-114">EXAMPLES</span></span>

### <span data-ttu-id="77657-115">Örnek 1: Tümleştirme hesabı şemasını oluşturma</span><span class="sxs-lookup"><span data-stu-id="77657-115">Example 1: Create the integration account schema</span></span>
```
PS C:\>New-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema1" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema1
Name        : IntegrationAccountSchema1
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="77657-116">Bu komut, belirtilen kaynak grubunda IntegrationAccountSchema1 adlı tümleştirme hesabı şemasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="77657-116">This command creates the integration account schema named IntegrationAccountSchema1 in the specified resource group.</span></span>

## <span data-ttu-id="77657-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="77657-117">PARAMETERS</span></span>

### <span data-ttu-id="77657-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="77657-118">-ContentType</span></span>
<span data-ttu-id="77657-119">Tümleştirme hesabı şemasının içerik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="77657-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="77657-120">Bu cmdlet, harita içerik türü olarak Application/XML destekler.</span><span class="sxs-lookup"><span data-stu-id="77657-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="77657-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77657-121">-DefaultProfile</span></span>
<span data-ttu-id="77657-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="77657-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77657-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="77657-123">-Metadata</span></span>
<span data-ttu-id="77657-124">Şema için bir meta veri nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="77657-124">Specifies a metadata object for the schema.</span></span>

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

### <span data-ttu-id="77657-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="77657-125">-Name</span></span>
<span data-ttu-id="77657-126">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="77657-126">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="77657-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77657-127">-ResourceGroupName</span></span>
<span data-ttu-id="77657-128">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="77657-128">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="77657-129">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="77657-129">-SchemaDefinition</span></span>
<span data-ttu-id="77657-130">Tümleştirme hesabı şeması için bir tanım nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="77657-130">Specifies a definition object for integration account schema.</span></span>
<span data-ttu-id="77657-131">Bu parametreyi veya *Schemafilepath* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="77657-131">Specify either this parameter or the *SchemaFilePath* parameter.</span></span>

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

### <span data-ttu-id="77657-132">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="77657-132">-SchemaFilePath</span></span>
<span data-ttu-id="77657-133">Tümleştirme hesabı şemasının bir tanımının dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="77657-133">Specifies the file path of a definition for the integration account schema.</span></span>
<span data-ttu-id="77657-134">Bu parametreyi veya *Schemadefinition* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="77657-134">Specify either this parameter or the *SchemaDefinition* parameter.</span></span>

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

### <span data-ttu-id="77657-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="77657-135">-SchemaName</span></span>
<span data-ttu-id="77657-136">Tümleştirme hesabı şemasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="77657-136">Specifies a name for the integration account schema.</span></span>

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

### <span data-ttu-id="77657-137">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="77657-137">-SchemaType</span></span>
<span data-ttu-id="77657-138">Tümleştirme hesabı şemasının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="77657-138">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="77657-139">Bu parametre, tür olarak XML 'i destekler.</span><span class="sxs-lookup"><span data-stu-id="77657-139">This parameter supports Xml as the type.</span></span>

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

### <span data-ttu-id="77657-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="77657-140">-Confirm</span></span>
<span data-ttu-id="77657-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="77657-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77657-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77657-142">-WhatIf</span></span>
<span data-ttu-id="77657-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="77657-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77657-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="77657-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77657-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77657-145">CommonParameters</span></span>
<span data-ttu-id="77657-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="77657-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77657-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77657-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77657-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="77657-148">INPUTS</span></span>

### <span data-ttu-id="77657-149">System. String</span><span class="sxs-lookup"><span data-stu-id="77657-149">System.String</span></span>

## <span data-ttu-id="77657-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="77657-150">OUTPUTS</span></span>

### <span data-ttu-id="77657-151">Microsoft. Azure. Management. Logic. modeller. ıntegrationaccountschema</span><span class="sxs-lookup"><span data-stu-id="77657-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="77657-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="77657-152">NOTES</span></span>

## <span data-ttu-id="77657-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="77657-153">RELATED LINKS</span></span>

[<span data-ttu-id="77657-154">Get-Azıntegrationaccountschema</span><span class="sxs-lookup"><span data-stu-id="77657-154">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="77657-155">Remove-Azıntegrationaccountschema</span><span class="sxs-lookup"><span data-stu-id="77657-155">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)

[<span data-ttu-id="77657-156">Set-Azıntegrationaccountschema</span><span class="sxs-lookup"><span data-stu-id="77657-156">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


