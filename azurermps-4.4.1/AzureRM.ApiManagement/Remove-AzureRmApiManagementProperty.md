---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D3C60123-CE1F-45F1-8C8F-25CDC302490C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProperty.md
ms.openlocfilehash: 333ed1cb778a5a366a7ad26d426559399658db1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587027"
---
# <span data-ttu-id="638ce-101">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="638ce-101">Remove-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="638ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="638ce-102">SYNOPSIS</span></span>
<span data-ttu-id="638ce-103">Bir API yönetim özelliğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="638ce-103">Removes an API Management Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="638ce-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="638ce-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="638ce-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="638ce-105">DESCRIPTION</span></span>
<span data-ttu-id="638ce-106">**Remove-Azurermapsananagementproperty** cmdlet 'ı BIR Azure API Yönetim **özelliğini** kaldırır.</span><span class="sxs-lookup"><span data-stu-id="638ce-106">The **Remove-AzureRmApiManagementProperty** cmdlet removes an Azure API Management **Property**.</span></span>

## <span data-ttu-id="638ce-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="638ce-107">EXAMPLES</span></span>

### <span data-ttu-id="638ce-108">Örnek 1: Özellik Kaldırma</span><span class="sxs-lookup"><span data-stu-id="638ce-108">Example 1: Remove a property</span></span>
```
PS C:\>Remove-AzureRmApiManagementProperty -Context $ApimContext -PropertyId "Property11" -PassThru
```

<span data-ttu-id="638ce-109">Bu komut, KIMLIK Property11 özelliğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="638ce-109">This command removes the property that has the ID Property11.</span></span>

## <span data-ttu-id="638ce-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="638ce-110">PARAMETERS</span></span>

### <span data-ttu-id="638ce-111">-Context</span><span class="sxs-lookup"><span data-stu-id="638ce-111">-Context</span></span>
<span data-ttu-id="638ce-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="638ce-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="638ce-113">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="638ce-113">-PassThru</span></span>
<span data-ttu-id="638ce-114">İşlem başarılı olduğunda, bu cmdlet 'in bir $True değeri döndürmeyeceğini gösterir veya aksi takdirde $False.</span><span class="sxs-lookup"><span data-stu-id="638ce-114">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="638ce-115">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="638ce-115">-PropertyId</span></span>
<span data-ttu-id="638ce-116">Bu cmdlet 'in kaldırıldığı özelliğin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="638ce-116">Specifies an ID of the property that this cmdlet removes.</span></span>

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

### <span data-ttu-id="638ce-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="638ce-117">-Confirm</span></span>
<span data-ttu-id="638ce-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="638ce-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="638ce-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="638ce-119">-WhatIf</span></span>
<span data-ttu-id="638ce-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="638ce-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="638ce-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="638ce-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="638ce-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="638ce-122">-DefaultProfile</span></span>
<span data-ttu-id="638ce-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="638ce-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="638ce-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="638ce-124">CommonParameters</span></span>
<span data-ttu-id="638ce-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="638ce-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="638ce-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="638ce-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="638ce-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="638ce-127">INPUTS</span></span>

## <span data-ttu-id="638ce-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="638ce-128">OUTPUTS</span></span>

### <span data-ttu-id="638ce-129">bool</span><span class="sxs-lookup"><span data-stu-id="638ce-129">bool</span></span>

## <span data-ttu-id="638ce-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="638ce-130">NOTES</span></span>

## <span data-ttu-id="638ce-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="638ce-131">RELATED LINKS</span></span>

[<span data-ttu-id="638ce-132">New-Azurermapsananagementproperty</span><span class="sxs-lookup"><span data-stu-id="638ce-132">New-AzureRmApiManagementProperty</span></span>](./New-AzureRmApiManagementProperty.md)

[<span data-ttu-id="638ce-133">Set-Azurermapımanagementproperty</span><span class="sxs-lookup"><span data-stu-id="638ce-133">Set-AzureRmApiManagementProperty</span></span>](./Set-AzureRmApiManagementProperty.md)


