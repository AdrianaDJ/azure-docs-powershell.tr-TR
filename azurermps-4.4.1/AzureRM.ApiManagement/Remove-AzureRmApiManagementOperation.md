---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
ms.openlocfilehash: 685da9955f272066ec39890ea0f3a063d3b2f9b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588015"
---
# <span data-ttu-id="10e7a-101">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="10e7a-101">Remove-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="10e7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10e7a-102">SYNOPSIS</span></span>
<span data-ttu-id="10e7a-103">Var olan bir işlemi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="10e7a-103">Removes an existing operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10e7a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="10e7a-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10e7a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="10e7a-105">DESCRIPTION</span></span>
<span data-ttu-id="10e7a-106">**Remove-Azurermapsananagementoperation** cmdlet 'i var olan bir işlemi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="10e7a-106">The **Remove-AzureRmApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="10e7a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="10e7a-107">EXAMPLES</span></span>

### <span data-ttu-id="10e7a-108">Örnek 1: var olan bir API Işlemini kaldırma</span><span class="sxs-lookup"><span data-stu-id="10e7a-108">Example 1: Remove an existing API Operation</span></span>
```
PS C:\>Remove-AzureRmApiManagementOperation -Context $APImContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="10e7a-109">Bu komut, var olan bir API Işlemini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="10e7a-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="10e7a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="10e7a-110">PARAMETERS</span></span>

### <span data-ttu-id="10e7a-111">-Apııd</span><span class="sxs-lookup"><span data-stu-id="10e7a-111">-ApiId</span></span>
<span data-ttu-id="10e7a-112">API 'nin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="10e7a-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="10e7a-113">-Context</span><span class="sxs-lookup"><span data-stu-id="10e7a-113">-Context</span></span>
<span data-ttu-id="10e7a-114">**Psapsananagementcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="10e7a-114">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10e7a-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="10e7a-115">-OperationId</span></span>
<span data-ttu-id="10e7a-116">API işleminin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="10e7a-116">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="10e7a-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="10e7a-117">-PassThru</span></span>
<span data-ttu-id="10e7a-118">Bu cmdlet 'in başarılı olduğu bir $True değerini veya $False değerini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="10e7a-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10e7a-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="10e7a-119">-Confirm</span></span>
<span data-ttu-id="10e7a-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="10e7a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10e7a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10e7a-121">-WhatIf</span></span>
<span data-ttu-id="10e7a-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="10e7a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10e7a-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="10e7a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10e7a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10e7a-124">-DefaultProfile</span></span>
<span data-ttu-id="10e7a-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="10e7a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10e7a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10e7a-126">CommonParameters</span></span>
<span data-ttu-id="10e7a-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="10e7a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10e7a-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10e7a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10e7a-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="10e7a-129">INPUTS</span></span>

## <span data-ttu-id="10e7a-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="10e7a-130">OUTPUTS</span></span>

### <span data-ttu-id="10e7a-131">bool</span><span class="sxs-lookup"><span data-stu-id="10e7a-131">bool</span></span>

## <span data-ttu-id="10e7a-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="10e7a-132">NOTES</span></span>

## <span data-ttu-id="10e7a-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="10e7a-133">RELATED LINKS</span></span>

[<span data-ttu-id="10e7a-134">Get-Azurermapsananama</span><span class="sxs-lookup"><span data-stu-id="10e7a-134">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="10e7a-135">Yeni-Azurermapsananaks</span><span class="sxs-lookup"><span data-stu-id="10e7a-135">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="10e7a-136">Set-Azurermapımanagementoperation</span><span class="sxs-lookup"><span data-stu-id="10e7a-136">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


