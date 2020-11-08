---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiSchema.md
ms.openlocfilehash: 7b28a9ff44251e84656411d6322eb87eac9f4991
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097427"
---
# <span data-ttu-id="e9370-101">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="e9370-101">Get-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="e9370-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9370-102">SYNOPSIS</span></span>
<span data-ttu-id="e9370-103">API şemasının ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="e9370-103">Get the details of the API Schema</span></span>

## <span data-ttu-id="e9370-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e9370-104">SYNTAX</span></span>

### <span data-ttu-id="e9370-105">ContextParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e9370-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9370-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e9370-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiSchema -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9370-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e9370-107">DESCRIPTION</span></span>
<span data-ttu-id="e9370-108">**Get-AzApiManagementApiSchema** CMDLET 'ı API şemasının ayrıntılarını alır</span><span class="sxs-lookup"><span data-stu-id="e9370-108">The **Get-AzApiManagementApiSchema** cmdlet gets the details of the API Schema</span></span>

## <span data-ttu-id="e9370-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e9370-109">EXAMPLES</span></span>

### <span data-ttu-id="e9370-110">Örnek 1: API 'nin tüm API şemasının ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="e9370-110">Example 1 : Get the details of all the Api Schema of an Api</span></span>
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

<span data-ttu-id="e9370-111">Bu komut, `swagger-petstore-extensive` belirli bir anlık içerik Için API ile ilişkilendirilmiş tüm API şemalarını alır.</span><span class="sxs-lookup"><span data-stu-id="e9370-111">This command gets all the API schemas associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

### <span data-ttu-id="e9370-112">Örnek 2: API ile ilişkilendirilmiş belirli bir şemayı alma</span><span class="sxs-lookup"><span data-stu-id="e9370-112">Example 2 : Get the specific schema associated with an Api</span></span>
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

<span data-ttu-id="e9370-113">Bu komut, `5cc9cf67e6ed3b1154e638bd` `swagger-petstore-extensive` belirli bir Apımanama bağlamı için API Ile ilişkilendirilmiş API şemasını alır.</span><span class="sxs-lookup"><span data-stu-id="e9370-113">This command gets the API schema `5cc9cf67e6ed3b1154e638bd` associated with an Api `swagger-petstore-extensive` for particular ApiManagement Context.</span></span>

## <span data-ttu-id="e9370-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e9370-114">PARAMETERS</span></span>

### <span data-ttu-id="e9370-115">-Apııd</span><span class="sxs-lookup"><span data-stu-id="e9370-115">-ApiId</span></span>
<span data-ttu-id="e9370-116">Bakılacak API tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="e9370-116">API identifier to look for.</span></span>
<span data-ttu-id="e9370-117">Belirtilmişse kimliği kullanarak API 'YI almayı dener.</span><span class="sxs-lookup"><span data-stu-id="e9370-117">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="e9370-118">-Context</span><span class="sxs-lookup"><span data-stu-id="e9370-118">-Context</span></span>
<span data-ttu-id="e9370-119">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="e9370-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e9370-120">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="e9370-120">This parameter is required.</span></span>

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

### <span data-ttu-id="e9370-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9370-121">-DefaultProfile</span></span>
<span data-ttu-id="e9370-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e9370-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9370-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e9370-123">-ResourceId</span></span>
<span data-ttu-id="e9370-124">Bir API şemasının ARM kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="e9370-124">Arm Resource Identifier of a Api Schema.</span></span> <span data-ttu-id="e9370-125">Belirtilmişse tanımlayıcıya göre API şemasını bulmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="e9370-125">If specified will try to find api schema by the identifier.</span></span> <span data-ttu-id="e9370-126">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="e9370-126">This parameter is required.</span></span>

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

### <span data-ttu-id="e9370-127">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="e9370-127">-SchemaId</span></span>
<span data-ttu-id="e9370-128">Şemanın tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="e9370-128">The identifier of the Schema.</span></span>

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

### <span data-ttu-id="e9370-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9370-129">CommonParameters</span></span>
<span data-ttu-id="e9370-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e9370-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9370-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e9370-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9370-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e9370-132">INPUTS</span></span>

### <span data-ttu-id="e9370-133">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="e9370-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e9370-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e9370-134">System.String</span></span>

## <span data-ttu-id="e9370-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e9370-135">OUTPUTS</span></span>

### <span data-ttu-id="e9370-136">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="e9370-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="e9370-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e9370-137">NOTES</span></span>

## <span data-ttu-id="e9370-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e9370-138">RELATED LINKS</span></span>

[<span data-ttu-id="e9370-139">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="e9370-139">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="e9370-140">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="e9370-140">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="e9370-141">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="e9370-141">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)