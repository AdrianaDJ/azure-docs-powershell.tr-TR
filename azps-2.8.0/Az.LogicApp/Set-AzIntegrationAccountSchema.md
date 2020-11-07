---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 3D4E44E3-0B55-4699-944F-412EE80CEEEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountSchema.md
ms.openlocfilehash: 99cbaa3b6b1c6fc471c98abee1953049d06f904b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751479"
---
# <span data-ttu-id="de5d4-101">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="de5d4-101">Set-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="de5d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de5d4-102">SYNOPSIS</span></span>
<span data-ttu-id="de5d4-103">Tümleştirme hesabı şemasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="de5d4-103">Modifies an integration account schema.</span></span>

## <span data-ttu-id="de5d4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="de5d4-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="de5d4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="de5d4-105">DESCRIPTION</span></span>
<span data-ttu-id="de5d4-106">**Set-Azıntegrationaccountschema** cmdlet 'i bir tümleştirme hesabı şemasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="de5d4-106">The **Set-AzIntegrationAccountSchema** cmdlet modifies an integration account schema.</span></span>
<span data-ttu-id="de5d4-107">Bu cmdlet, tümleştirme hesabı şemasını temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="de5d4-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="de5d4-108">Tümleştirme hesap adını, kaynak grubu adını ve şema adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="de5d4-108">Specify the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="de5d4-109">Komut satırında belirttiğiniz şablon parametre dosyası değerleri, bir şablon parametre nesnesindeki şablon parametre değerlerinden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="de5d4-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="de5d4-110">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="de5d4-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="de5d4-111">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="de5d4-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="de5d4-112">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="de5d4-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="de5d4-113">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="de5d4-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="de5d4-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="de5d4-114">EXAMPLES</span></span>

### <span data-ttu-id="de5d4-115">Örnek 1: Tümleştirme hesabı şemasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="de5d4-115">Example 1: Modify an integration account schema</span></span>
```
PS C:\>Set-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name        : IntegrationAccountSchema43
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="de5d4-116">Bu komut, IntegrationAccountSchema43 adlı tümleştirme hesabı şemasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="de5d4-116">This command modifies the integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="de5d4-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="de5d4-117">PARAMETERS</span></span>

### <span data-ttu-id="de5d4-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="de5d4-118">-ContentType</span></span>
<span data-ttu-id="de5d4-119">Tümleştirme hesabı şemasının içerik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="de5d4-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="de5d4-120">Bu cmdlet, harita içerik türü olarak Application/XML destekler.</span><span class="sxs-lookup"><span data-stu-id="de5d4-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="de5d4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de5d4-121">-DefaultProfile</span></span>
<span data-ttu-id="de5d4-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="de5d4-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de5d4-123">-Force</span><span class="sxs-lookup"><span data-stu-id="de5d4-123">-Force</span></span>
<span data-ttu-id="de5d4-124">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="de5d4-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="de5d4-125">-Metadata</span><span class="sxs-lookup"><span data-stu-id="de5d4-125">-Metadata</span></span>
<span data-ttu-id="de5d4-126">Şema için bir meta veri nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="de5d4-126">Specifies a metadata object for the schema.</span></span>

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

### <span data-ttu-id="de5d4-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="de5d4-127">-Name</span></span>
<span data-ttu-id="de5d4-128">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="de5d4-128">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="de5d4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de5d4-129">-ResourceGroupName</span></span>
<span data-ttu-id="de5d4-130">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="de5d4-130">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="de5d4-131">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="de5d4-131">-SchemaDefinition</span></span>
<span data-ttu-id="de5d4-132">Tümleştirme hesabı şeması için bir tanım nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="de5d4-132">Specifies a definition object for integration account schema.</span></span>

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

### <span data-ttu-id="de5d4-133">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="de5d4-133">-SchemaFilePath</span></span>
<span data-ttu-id="de5d4-134">Tümleştirme hesabı şemasının bir tanımının dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="de5d4-134">Specifies the file path of a definition for the integration account schema.</span></span>

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

### <span data-ttu-id="de5d4-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="de5d4-135">-SchemaName</span></span>
<span data-ttu-id="de5d4-136">Tümleştirme hesabı şemasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="de5d4-136">Specifies the name of the integration account schema.</span></span>

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

### <span data-ttu-id="de5d4-137">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="de5d4-137">-SchemaType</span></span>
<span data-ttu-id="de5d4-138">Tümleştirme hesabı şemasının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="de5d4-138">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="de5d4-139">Bu parametre, tür olarak XML 'i destekler.</span><span class="sxs-lookup"><span data-stu-id="de5d4-139">This parameter supports Xml as the type.</span></span>

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

### <span data-ttu-id="de5d4-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="de5d4-140">-Confirm</span></span>
<span data-ttu-id="de5d4-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="de5d4-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de5d4-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de5d4-142">-WhatIf</span></span>
<span data-ttu-id="de5d4-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="de5d4-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de5d4-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="de5d4-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de5d4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de5d4-145">CommonParameters</span></span>
<span data-ttu-id="de5d4-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="de5d4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de5d4-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de5d4-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de5d4-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="de5d4-148">INPUTS</span></span>

### <span data-ttu-id="de5d4-149">System. String</span><span class="sxs-lookup"><span data-stu-id="de5d4-149">System.String</span></span>

## <span data-ttu-id="de5d4-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="de5d4-150">OUTPUTS</span></span>

### <span data-ttu-id="de5d4-151">Microsoft. Azure. Management. Logic. modeller. ıntegrationaccountschema</span><span class="sxs-lookup"><span data-stu-id="de5d4-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="de5d4-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="de5d4-152">NOTES</span></span>

## <span data-ttu-id="de5d4-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="de5d4-153">RELATED LINKS</span></span>

[<span data-ttu-id="de5d4-154">Get-Azıntegrationaccountschema</span><span class="sxs-lookup"><span data-stu-id="de5d4-154">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="de5d4-155">Yeni-Azıntegrationaccountschema</span><span class="sxs-lookup"><span data-stu-id="de5d4-155">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="de5d4-156">Remove-Azıntegrationaccountschema</span><span class="sxs-lookup"><span data-stu-id="de5d4-156">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)


