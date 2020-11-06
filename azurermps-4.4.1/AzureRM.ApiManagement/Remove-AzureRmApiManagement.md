---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
ms.openlocfilehash: 5a46e75f7ce7b0639de015de975c321c9d5c1ed6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587036"
---
# <span data-ttu-id="8028c-101">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="8028c-101">Remove-AzureRmApiManagement</span></span>

## <span data-ttu-id="8028c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8028c-102">SYNOPSIS</span></span>
<span data-ttu-id="8028c-103">Bir API Yönetim hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8028c-103">Removes an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8028c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8028c-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8028c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8028c-105">DESCRIPTION</span></span>
<span data-ttu-id="8028c-106">**Remove-Azurermapsananayönetii** cmdlet 'ı BIR Azure API Yönetim hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8028c-106">The **Remove-AzureRmApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="8028c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8028c-107">EXAMPLES</span></span>

### <span data-ttu-id="8028c-108">Örnek 1: bir API Yönetim hizmetini kaldırma</span><span class="sxs-lookup"><span data-stu-id="8028c-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="8028c-109">Bu komut, Contosoapı adlı API Yönetim hizmetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8028c-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="8028c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8028c-110">PARAMETERS</span></span>

### <span data-ttu-id="8028c-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="8028c-111">-Name</span></span>
<span data-ttu-id="8028c-112">Bu cmdlet 'in kaldırıldığı API yönetim dağıtımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8028c-112">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8028c-113">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8028c-113">-PassThru</span></span>
<span data-ttu-id="8028c-114">İşlem başarılı olursa bu cmdlet 'in bir $True değeri döndürmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8028c-114">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

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

### <span data-ttu-id="8028c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8028c-115">-ResourceGroupName</span></span>
<span data-ttu-id="8028c-116">API yönetim dağıtımının olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8028c-116">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="8028c-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="8028c-117">-Confirm</span></span>
<span data-ttu-id="8028c-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8028c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8028c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8028c-119">-WhatIf</span></span>
<span data-ttu-id="8028c-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8028c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8028c-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8028c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8028c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8028c-122">-DefaultProfile</span></span>
<span data-ttu-id="8028c-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8028c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8028c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8028c-124">CommonParameters</span></span>
<span data-ttu-id="8028c-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8028c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8028c-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8028c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8028c-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8028c-127">INPUTS</span></span>

## <span data-ttu-id="8028c-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8028c-128">OUTPUTS</span></span>

### <span data-ttu-id="8028c-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8028c-129">System.Boolean</span></span>

## <span data-ttu-id="8028c-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8028c-130">NOTES</span></span>

## <span data-ttu-id="8028c-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8028c-131">RELATED LINKS</span></span>

[<span data-ttu-id="8028c-132">Yedek-azurermapı</span><span class="sxs-lookup"><span data-stu-id="8028c-132">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="8028c-133">Get-azurermapı</span><span class="sxs-lookup"><span data-stu-id="8028c-133">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="8028c-134">Yeni-azurermapı</span><span class="sxs-lookup"><span data-stu-id="8028c-134">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="8028c-135">Geri yükleme-azurermapı</span><span class="sxs-lookup"><span data-stu-id="8028c-135">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


