---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagement.md
ms.openlocfilehash: 73f30ef12270ce738341e71b0428befe6a3a3ba5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917812"
---
# <span data-ttu-id="22186-101">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="22186-101">Remove-AzApiManagement</span></span>

## <span data-ttu-id="22186-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22186-102">SYNOPSIS</span></span>
<span data-ttu-id="22186-103">Bir API Yönetim hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="22186-103">Removes an API Management service.</span></span>

## <span data-ttu-id="22186-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="22186-104">SYNTAX</span></span>

```
Remove-AzApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22186-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="22186-105">DESCRIPTION</span></span>
<span data-ttu-id="22186-106">**Remove-Azapsananayönetii** cmdlet 'ı BIR Azure API Yönetim hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="22186-106">The **Remove-AzApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="22186-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="22186-107">EXAMPLES</span></span>

### <span data-ttu-id="22186-108">Örnek 1: bir API Yönetim hizmetini kaldırma</span><span class="sxs-lookup"><span data-stu-id="22186-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="22186-109">Bu komut, Contosoapı adlı API Yönetim hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="22186-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="22186-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="22186-110">PARAMETERS</span></span>

### <span data-ttu-id="22186-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22186-111">-DefaultProfile</span></span>
<span data-ttu-id="22186-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="22186-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22186-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="22186-113">-Name</span></span>
<span data-ttu-id="22186-114">Bu cmdlet 'in kaldırıldığı API yönetim dağıtımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="22186-114">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="22186-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="22186-115">-PassThru</span></span>
<span data-ttu-id="22186-116">İşlem başarılı olursa bu cmdlet 'in bir $True değeri döndürmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="22186-116">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

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

### <span data-ttu-id="22186-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22186-117">-ResourceGroupName</span></span>
<span data-ttu-id="22186-118">API yönetim dağıtımının olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="22186-118">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="22186-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="22186-119">-Confirm</span></span>
<span data-ttu-id="22186-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="22186-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22186-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22186-121">-WhatIf</span></span>
<span data-ttu-id="22186-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="22186-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22186-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="22186-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22186-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22186-124">CommonParameters</span></span>
<span data-ttu-id="22186-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="22186-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22186-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22186-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22186-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="22186-127">INPUTS</span></span>

### <span data-ttu-id="22186-128">System. String</span><span class="sxs-lookup"><span data-stu-id="22186-128">System.String</span></span>

## <span data-ttu-id="22186-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="22186-129">OUTPUTS</span></span>

### <span data-ttu-id="22186-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="22186-130">System.Boolean</span></span>

## <span data-ttu-id="22186-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="22186-131">NOTES</span></span>

## <span data-ttu-id="22186-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="22186-132">RELATED LINKS</span></span>

[<span data-ttu-id="22186-133">Yedek-azlı bir</span><span class="sxs-lookup"><span data-stu-id="22186-133">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="22186-134">Get-Azıbir</span><span class="sxs-lookup"><span data-stu-id="22186-134">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="22186-135">Yeni-azlı bir</span><span class="sxs-lookup"><span data-stu-id="22186-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="22186-136">Geri yükleme-azbir</span><span class="sxs-lookup"><span data-stu-id="22186-136">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


