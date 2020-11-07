---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
ms.openlocfilehash: cee512445f457e7353d5766cd561788b00360b40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763923"
---
# <span data-ttu-id="22d06-101">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="22d06-101">Remove-AzureRmApiManagement</span></span>

## <span data-ttu-id="22d06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22d06-102">SYNOPSIS</span></span>
<span data-ttu-id="22d06-103">Bir API Yönetim hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="22d06-103">Removes an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22d06-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="22d06-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22d06-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="22d06-105">DESCRIPTION</span></span>
<span data-ttu-id="22d06-106">**Remove-Azurermapsananayönetii** cmdlet 'ı BIR Azure API Yönetim hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="22d06-106">The **Remove-AzureRmApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="22d06-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="22d06-107">EXAMPLES</span></span>

### <span data-ttu-id="22d06-108">Örnek 1: bir API Yönetim hizmetini kaldırma</span><span class="sxs-lookup"><span data-stu-id="22d06-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="22d06-109">Bu komut, Contosoapı adlı API Yönetim hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="22d06-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="22d06-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="22d06-110">PARAMETERS</span></span>

### <span data-ttu-id="22d06-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22d06-111">-DefaultProfile</span></span>
<span data-ttu-id="22d06-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="22d06-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22d06-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="22d06-113">-Name</span></span>
<span data-ttu-id="22d06-114">Bu cmdlet 'in kaldırıldığı API yönetim dağıtımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="22d06-114">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="22d06-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="22d06-115">-PassThru</span></span>
<span data-ttu-id="22d06-116">İşlem başarılı olursa bu cmdlet 'in bir $True değeri döndürmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="22d06-116">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

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

### <span data-ttu-id="22d06-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22d06-117">-ResourceGroupName</span></span>
<span data-ttu-id="22d06-118">API yönetim dağıtımının olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="22d06-118">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="22d06-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="22d06-119">-Confirm</span></span>
<span data-ttu-id="22d06-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="22d06-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22d06-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22d06-121">-WhatIf</span></span>
<span data-ttu-id="22d06-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="22d06-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22d06-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="22d06-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22d06-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22d06-124">CommonParameters</span></span>
<span data-ttu-id="22d06-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="22d06-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22d06-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22d06-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22d06-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="22d06-127">INPUTS</span></span>

### <span data-ttu-id="22d06-128">System. String</span><span class="sxs-lookup"><span data-stu-id="22d06-128">System.String</span></span>

## <span data-ttu-id="22d06-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="22d06-129">OUTPUTS</span></span>

### <span data-ttu-id="22d06-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="22d06-130">System.Boolean</span></span>

## <span data-ttu-id="22d06-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="22d06-131">NOTES</span></span>

## <span data-ttu-id="22d06-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="22d06-132">RELATED LINKS</span></span>

[<span data-ttu-id="22d06-133">Yedek-azurermapı</span><span class="sxs-lookup"><span data-stu-id="22d06-133">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="22d06-134">Get-azurermapı</span><span class="sxs-lookup"><span data-stu-id="22d06-134">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="22d06-135">Yeni-azurermapı</span><span class="sxs-lookup"><span data-stu-id="22d06-135">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="22d06-136">Geri yükleme-azurermapı</span><span class="sxs-lookup"><span data-stu-id="22d06-136">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


