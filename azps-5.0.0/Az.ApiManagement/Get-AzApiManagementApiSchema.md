---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
ms.openlocfilehash: 837494b8f042d3ea788eda69d47845b02859c805
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324085"
---
# <span data-ttu-id="2a178-101">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="2a178-101">Get-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="2a178-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a178-102">SYNOPSIS</span></span>
<span data-ttu-id="2a178-103">API şemasının ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="2a178-103">Get the details of the API Schema</span></span>

## <span data-ttu-id="2a178-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2a178-104">SYNTAX</span></span>

### <span data-ttu-id="2a178-105">ContextParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2a178-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a178-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="2a178-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiSchema -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2a178-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2a178-107">DESCRIPTION</span></span>
<span data-ttu-id="2a178-108">**Get-AzApiManagementApiSchema** CMDLET 'ı API şemasının ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="2a178-108">The **Get-AzApiManagementApiSchema** cmdlet gets the details of the API Schema</span></span>

## <span data-ttu-id="2a178-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2a178-109">EXAMPLES</span></span>

### <span data-ttu-id="2a178-110">Örnek 1: API 'nin tüm API şemasının ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="2a178-110">Example 1: Get the details of all the Api Schema of an Api</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> Get-AzApiManagementApiSchema -Context $context -ApiId wsdlapitest

SchemaId           : 2a03e1b4-1826-4e59-b372-4711f575db28
Api Id             : wsdlapitest
Schema ContentType : xsdschema
Schema Document    : <s:schema elementFormDefault="qualified"....

SchemaId           : b6e5497d-f65a-4851-9f5b-b5684cdae688
Api Id             : wsdlapitest
Schema ContentType : xsdschema
Schema Document    : <?xml version=""1.0"" encoding=""UTF-8""....
```

<span data-ttu-id="2a178-111">Bu komut, `swagger-petstore-extensive` belirli bir anlık içerik Için API ile ilişkilendirilmiş tüm API şemalarını alır.</span><span class="sxs-lookup"><span data-stu-id="2a178-111">This command gets all the API schemas associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

### <span data-ttu-id="2a178-112">Örnek 2: API ile ilişkilendirilmiş belirli bir şemayı alma</span><span class="sxs-lookup"><span data-stu-id="2a178-112">Example 2: Get the specific schema associated with an Api</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> Get-AzApiManagementApiSchema -Context $context -ApiId swagger-petstore-extensive -SchemaId 5cc9cf67e6ed3b1154e638bd

SchemaId           : 5cc9cf67e6ed3b1154e638bd
Api Id             : swagger-petstore-extensive
Schema ContentType : swaggerdefinition
Schema Document    : {
                       "definitions": {
                         "pet": {
                        ....
```

<span data-ttu-id="2a178-113">Bu komut, `5cc9cf67e6ed3b1154e638bd` `swagger-petstore-extensive` belirli bir Apımanama bağlamı için API Ile ilişkilendirilmiş API şemasını alır.</span><span class="sxs-lookup"><span data-stu-id="2a178-113">This command gets the API schema `5cc9cf67e6ed3b1154e638bd` associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

## <span data-ttu-id="2a178-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2a178-114">PARAMETERS</span></span>

### <span data-ttu-id="2a178-115">-Apııd</span><span class="sxs-lookup"><span data-stu-id="2a178-115">-ApiId</span></span>
<span data-ttu-id="2a178-116">Bakılacak API tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="2a178-116">API identifier to look for.</span></span>
<span data-ttu-id="2a178-117">Belirtilmişse kimliği kullanarak API 'YI almayı dener.</span><span class="sxs-lookup"><span data-stu-id="2a178-117">If specified will try to get the API by the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a178-118">-Context</span><span class="sxs-lookup"><span data-stu-id="2a178-118">-Context</span></span>
<span data-ttu-id="2a178-119">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="2a178-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2a178-120">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2a178-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a178-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a178-121">-DefaultProfile</span></span>
<span data-ttu-id="2a178-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2a178-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a178-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2a178-123">-ResourceId</span></span>
<span data-ttu-id="2a178-124">Bir API şemasının ARM kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="2a178-124">Arm Resource Identifier of a Api Schema.</span></span> <span data-ttu-id="2a178-125">Belirtilmişse tanımlayıcıya göre API şemasını bulmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="2a178-125">If specified will try to find api schema by the identifier.</span></span> <span data-ttu-id="2a178-126">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2a178-126">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a178-127">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="2a178-127">-SchemaId</span></span>
<span data-ttu-id="2a178-128">Şemanın tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="2a178-128">The identifier of the Schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a178-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a178-129">CommonParameters</span></span>
<span data-ttu-id="2a178-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2a178-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a178-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2a178-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a178-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2a178-132">INPUTS</span></span>

### <span data-ttu-id="2a178-133">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="2a178-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2a178-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2a178-134">System.String</span></span>

## <span data-ttu-id="2a178-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2a178-135">OUTPUTS</span></span>

### <span data-ttu-id="2a178-136">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="2a178-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="2a178-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2a178-137">NOTES</span></span>

## <span data-ttu-id="2a178-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2a178-138">RELATED LINKS</span></span>

[<span data-ttu-id="2a178-139">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="2a178-139">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="2a178-140">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="2a178-140">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="2a178-141">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="2a178-141">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)