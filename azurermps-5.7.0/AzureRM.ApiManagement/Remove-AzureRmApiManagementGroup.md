---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementGroup.md
ms.openlocfilehash: a5919959f038b94a27f373124377466926494337
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593765"
---
# <span data-ttu-id="cc00c-101">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="cc00c-101">Remove-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="cc00c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc00c-102">SYNOPSIS</span></span>
<span data-ttu-id="cc00c-103">Var olan bir API yönetim grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cc00c-103">Removes an existing API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc00c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cc00c-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc00c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cc00c-105">DESCRIPTION</span></span>
<span data-ttu-id="cc00c-106">**Remove-Azurermapsananagementgroup** cmdlet 'i var olan bir API yönetim grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cc00c-106">The **Remove-AzureRmApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="cc00c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cc00c-107">EXAMPLES</span></span>

### <span data-ttu-id="cc00c-108">Örnek 1: var olan bir yönetim grubunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="cc00c-108">Example 1: Remove an existing management group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="cc00c-109">Bu komut Group0001 adlı bir yönetim grubunu kaldırır ve kullanıcıya onay istemez.</span><span class="sxs-lookup"><span data-stu-id="cc00c-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="cc00c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cc00c-110">PARAMETERS</span></span>

### <span data-ttu-id="cc00c-111">-Context</span><span class="sxs-lookup"><span data-stu-id="cc00c-111">-Context</span></span>
<span data-ttu-id="cc00c-112">**Psapimanagementcontext** nesnesinin örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc00c-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc00c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc00c-113">-DefaultProfile</span></span>
<span data-ttu-id="cc00c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cc00c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc00c-115">-GroupID</span><span class="sxs-lookup"><span data-stu-id="cc00c-115">-GroupId</span></span>
<span data-ttu-id="cc00c-116">Yönetim grubunun tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc00c-116">Specifies the identifier of a management group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc00c-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="cc00c-117">-PassThru</span></span>
<span data-ttu-id="cc00c-118">Bu cmdlet 'in başarılı olduğu bir $True değerini veya $False değerini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc00c-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc00c-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="cc00c-119">-Confirm</span></span>
<span data-ttu-id="cc00c-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cc00c-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc00c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc00c-121">-WhatIf</span></span>
<span data-ttu-id="cc00c-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cc00c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc00c-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cc00c-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc00c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc00c-124">CommonParameters</span></span>
<span data-ttu-id="cc00c-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cc00c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc00c-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc00c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc00c-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cc00c-127">INPUTS</span></span>

### <span data-ttu-id="cc00c-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="cc00c-128">None</span></span>
<span data-ttu-id="cc00c-129">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="cc00c-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cc00c-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cc00c-130">OUTPUTS</span></span>

### <span data-ttu-id="cc00c-131">Boole</span><span class="sxs-lookup"><span data-stu-id="cc00c-131">Boolean</span></span>

## <span data-ttu-id="cc00c-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cc00c-132">NOTES</span></span>

## <span data-ttu-id="cc00c-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cc00c-133">RELATED LINKS</span></span>

[<span data-ttu-id="cc00c-134">Get-Azurermapımanagementgroup</span><span class="sxs-lookup"><span data-stu-id="cc00c-134">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="cc00c-135">Yeni-Azurermapımanagementgroup</span><span class="sxs-lookup"><span data-stu-id="cc00c-135">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="cc00c-136">Set-Azurermapımanagementgroup</span><span class="sxs-lookup"><span data-stu-id="cc00c-136">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


