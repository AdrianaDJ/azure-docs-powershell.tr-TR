---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
ms.openlocfilehash: 197b1605d178c0aaa1c3f96580cb295306910232
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594153"
---
# <span data-ttu-id="c93ba-101">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="c93ba-101">Remove-AzureRmApiManagement</span></span>

## <span data-ttu-id="c93ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c93ba-102">SYNOPSIS</span></span>
<span data-ttu-id="c93ba-103">Bir API Yönetim hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c93ba-103">Removes an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c93ba-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c93ba-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c93ba-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c93ba-105">DESCRIPTION</span></span>
<span data-ttu-id="c93ba-106">**Remove-Azurermapsananayönetii** cmdlet 'ı BIR Azure API Yönetim hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c93ba-106">The **Remove-AzureRmApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="c93ba-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c93ba-107">EXAMPLES</span></span>

### <span data-ttu-id="c93ba-108">Örnek 1: bir API Yönetim hizmetini kaldırma</span><span class="sxs-lookup"><span data-stu-id="c93ba-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="c93ba-109">Bu komut, Contosoapı adlı API Yönetim hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c93ba-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="c93ba-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c93ba-110">PARAMETERS</span></span>

### <span data-ttu-id="c93ba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c93ba-111">-DefaultProfile</span></span>
<span data-ttu-id="c93ba-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c93ba-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="c93ba-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="c93ba-113">-Name</span></span>
<span data-ttu-id="c93ba-114">Bu cmdlet 'in kaldırıldığı API yönetim dağıtımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c93ba-114">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c93ba-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c93ba-115">-PassThru</span></span>
<span data-ttu-id="c93ba-116">İşlem başarılı olursa bu cmdlet 'in bir $True değeri döndürmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c93ba-116">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c93ba-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c93ba-117">-ResourceGroupName</span></span>
<span data-ttu-id="c93ba-118">API yönetim dağıtımının olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c93ba-118">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="c93ba-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="c93ba-119">-Confirm</span></span>
<span data-ttu-id="c93ba-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c93ba-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c93ba-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c93ba-121">-WhatIf</span></span>
<span data-ttu-id="c93ba-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c93ba-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c93ba-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c93ba-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c93ba-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c93ba-124">CommonParameters</span></span>
<span data-ttu-id="c93ba-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c93ba-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c93ba-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c93ba-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c93ba-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c93ba-127">INPUTS</span></span>

### <span data-ttu-id="c93ba-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c93ba-128">None</span></span>
<span data-ttu-id="c93ba-129">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="c93ba-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c93ba-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c93ba-130">OUTPUTS</span></span>

### <span data-ttu-id="c93ba-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c93ba-131">System.Boolean</span></span>

## <span data-ttu-id="c93ba-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c93ba-132">NOTES</span></span>

## <span data-ttu-id="c93ba-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c93ba-133">RELATED LINKS</span></span>

[<span data-ttu-id="c93ba-134">Yedek-azurermapı</span><span class="sxs-lookup"><span data-stu-id="c93ba-134">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="c93ba-135">Get-azurermapı</span><span class="sxs-lookup"><span data-stu-id="c93ba-135">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="c93ba-136">Yeni-azurermapı</span><span class="sxs-lookup"><span data-stu-id="c93ba-136">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="c93ba-137">Geri yükleme-azurermapı</span><span class="sxs-lookup"><span data-stu-id="c93ba-137">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


