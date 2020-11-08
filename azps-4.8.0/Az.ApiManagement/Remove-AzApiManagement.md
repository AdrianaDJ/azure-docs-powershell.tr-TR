---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
ms.openlocfilehash: f54998dc0d5ec8570a573870148a8cf05c265618
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273760"
---
# <span data-ttu-id="3e71f-101">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="3e71f-101">Remove-AzApiManagement</span></span>

## <span data-ttu-id="3e71f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e71f-102">SYNOPSIS</span></span>
<span data-ttu-id="3e71f-103">Bir API Yönetim hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3e71f-103">Removes an API Management service.</span></span>

## <span data-ttu-id="3e71f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3e71f-104">SYNTAX</span></span>

```
Remove-AzApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e71f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3e71f-105">DESCRIPTION</span></span>
<span data-ttu-id="3e71f-106">**Remove-Azapsananayönetii** cmdlet 'ı BIR Azure API Yönetim hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3e71f-106">The **Remove-AzApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="3e71f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3e71f-107">EXAMPLES</span></span>

### <span data-ttu-id="3e71f-108">Örnek 1: bir API Yönetim hizmetini kaldırma</span><span class="sxs-lookup"><span data-stu-id="3e71f-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="3e71f-109">Bu komut, Contosoapı adlı API Yönetim hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3e71f-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="3e71f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3e71f-110">PARAMETERS</span></span>

### <span data-ttu-id="3e71f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e71f-111">-DefaultProfile</span></span>
<span data-ttu-id="3e71f-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3e71f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e71f-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="3e71f-113">-Name</span></span>
<span data-ttu-id="3e71f-114">Bu cmdlet 'in kaldırıldığı API yönetim dağıtımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e71f-114">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3e71f-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3e71f-115">-PassThru</span></span>
<span data-ttu-id="3e71f-116">İşlem başarılı olursa bu cmdlet 'in bir $True değeri döndürmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e71f-116">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

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

### <span data-ttu-id="3e71f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e71f-117">-ResourceGroupName</span></span>
<span data-ttu-id="3e71f-118">API yönetim dağıtımının olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e71f-118">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="3e71f-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="3e71f-119">-Confirm</span></span>
<span data-ttu-id="3e71f-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3e71f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e71f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e71f-121">-WhatIf</span></span>
<span data-ttu-id="3e71f-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3e71f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e71f-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3e71f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e71f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e71f-124">CommonParameters</span></span>
<span data-ttu-id="3e71f-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3e71f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e71f-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3e71f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e71f-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3e71f-127">INPUTS</span></span>

### <span data-ttu-id="3e71f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3e71f-128">System.String</span></span>

## <span data-ttu-id="3e71f-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3e71f-129">OUTPUTS</span></span>

### <span data-ttu-id="3e71f-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3e71f-130">System.Boolean</span></span>

## <span data-ttu-id="3e71f-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3e71f-131">NOTES</span></span>

## <span data-ttu-id="3e71f-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3e71f-132">RELATED LINKS</span></span>

[<span data-ttu-id="3e71f-133">Yedek-azlı bir</span><span class="sxs-lookup"><span data-stu-id="3e71f-133">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="3e71f-134">Get-Azıbir</span><span class="sxs-lookup"><span data-stu-id="3e71f-134">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="3e71f-135">Yeni-azlı bir</span><span class="sxs-lookup"><span data-stu-id="3e71f-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="3e71f-136">Geri yükleme-azbir</span><span class="sxs-lookup"><span data-stu-id="3e71f-136">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


