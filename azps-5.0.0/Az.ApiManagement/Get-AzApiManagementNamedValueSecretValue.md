---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvaluesecretvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValueSecretValue.md
ms.openlocfilehash: 5ec602e4cd86086a7be8e7ae53c1c2bb551a963c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324070"
---
# <span data-ttu-id="a7ef7-101">Get-AzApiManagementNamedValueSecretValue</span><span class="sxs-lookup"><span data-stu-id="a7ef7-101">Get-AzApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="a7ef7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7ef7-102">SYNOPSIS</span></span>
<span data-ttu-id="a7ef7-103">Belirli bir adlandırılmış değerin gizli değerini alır.</span><span class="sxs-lookup"><span data-stu-id="a7ef7-103">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="a7ef7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a7ef7-104">SYNTAX</span></span>

### <span data-ttu-id="a7ef7-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a7ef7-105">Default (Default)</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7ef7-106">Getbynamedvalueıd</span><span class="sxs-lookup"><span data-stu-id="a7ef7-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValueSecretValue -Context <PsApiManagementContext> -NamedValueId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7ef7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a7ef7-107">DESCRIPTION</span></span>
<span data-ttu-id="a7ef7-108">Belirli bir adlandırılmış değerin gizli değerini alır.</span><span class="sxs-lookup"><span data-stu-id="a7ef7-108">Gets a secret value of the particular Named Value.</span></span>

## <span data-ttu-id="a7ef7-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a7ef7-109">EXAMPLES</span></span>

### <span data-ttu-id="a7ef7-110">Örnek 1: ada göre adlandırılmış değeri alma</span><span class="sxs-lookup"><span data-stu-id="a7ef7-110">Example 1: Get named value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValueSecretValue -Context $apimContext -NamedValueId "sql-connectionstring"
```

<span data-ttu-id="a7ef7-111">Bu komut, adlandırılmış değer adı verilen değer ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="a7ef7-111">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="a7ef7-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a7ef7-112">PARAMETERS</span></span>

### <span data-ttu-id="a7ef7-113">-Context</span><span class="sxs-lookup"><span data-stu-id="a7ef7-113">-Context</span></span>
<span data-ttu-id="a7ef7-114">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="a7ef7-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a7ef7-115">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a7ef7-115">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7ef7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7ef7-116">-DefaultProfile</span></span>
<span data-ttu-id="a7ef7-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a7ef7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7ef7-118">Namedvalueıd</span><span class="sxs-lookup"><span data-stu-id="a7ef7-118">-NamedValueId</span></span>
<span data-ttu-id="a7ef7-119">Adlandırılmış değerin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="a7ef7-119">Identifier of a the named value.</span></span>
<span data-ttu-id="a7ef7-120">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a7ef7-120">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNamedValueId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7ef7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7ef7-121">CommonParameters</span></span>
<span data-ttu-id="a7ef7-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a7ef7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7ef7-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a7ef7-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7ef7-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a7ef7-124">INPUTS</span></span>

### <span data-ttu-id="a7ef7-125">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="a7ef7-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a7ef7-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a7ef7-126">System.String</span></span>

## <span data-ttu-id="a7ef7-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a7ef7-127">OUTPUTS</span></span>

### <span data-ttu-id="a7ef7-128">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementnamedvaluesecretvalue</span><span class="sxs-lookup"><span data-stu-id="a7ef7-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValueSecretValue</span></span>

## <span data-ttu-id="a7ef7-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a7ef7-129">NOTES</span></span>

## <span data-ttu-id="a7ef7-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a7ef7-130">RELATED LINKS</span></span>
