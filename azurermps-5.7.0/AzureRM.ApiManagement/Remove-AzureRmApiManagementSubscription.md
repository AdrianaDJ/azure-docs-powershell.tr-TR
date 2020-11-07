---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 777d71dec17f75cba84c15c7499e5ec56ffb854a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765125"
---
# <span data-ttu-id="6a156-101">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="6a156-101">Remove-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="6a156-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a156-102">SYNOPSIS</span></span>
<span data-ttu-id="6a156-103">Var olan bir aboneliği siler.</span><span class="sxs-lookup"><span data-stu-id="6a156-103">Deletes an existing subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a156-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6a156-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a156-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6a156-105">DESCRIPTION</span></span>
<span data-ttu-id="6a156-106">**Remove-Azurermapsananagementsubscription** cmdlet 'i var olan bir aboneliği siler.</span><span class="sxs-lookup"><span data-stu-id="6a156-106">The **Remove-AzureRmApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="6a156-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6a156-107">EXAMPLES</span></span>

### <span data-ttu-id="6a156-108">Örnek 1: aboneliği silme</span><span class="sxs-lookup"><span data-stu-id="6a156-108">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="6a156-109">Bu komut, var olan bir aboneliği siler.</span><span class="sxs-lookup"><span data-stu-id="6a156-109">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="6a156-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6a156-110">PARAMETERS</span></span>

### <span data-ttu-id="6a156-111">-Context</span><span class="sxs-lookup"><span data-stu-id="6a156-111">-Context</span></span>
<span data-ttu-id="6a156-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a156-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6a156-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a156-113">-DefaultProfile</span></span>
<span data-ttu-id="6a156-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6a156-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="6a156-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6a156-115">-PassThru</span></span>
<span data-ttu-id="6a156-116">Bu cmdlet 'in bir $True değerini (başarılı olursa), aksi takdirde $false değerini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a156-116">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="6a156-117">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="6a156-117">-SubscriptionId</span></span>
<span data-ttu-id="6a156-118">Abonelik KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a156-118">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="6a156-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="6a156-119">-Confirm</span></span>
<span data-ttu-id="6a156-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6a156-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a156-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a156-121">-WhatIf</span></span>
<span data-ttu-id="6a156-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6a156-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a156-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6a156-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a156-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a156-124">CommonParameters</span></span>
<span data-ttu-id="6a156-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6a156-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a156-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a156-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a156-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6a156-127">INPUTS</span></span>

### <span data-ttu-id="6a156-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6a156-128">None</span></span>
<span data-ttu-id="6a156-129">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="6a156-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6a156-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6a156-130">OUTPUTS</span></span>

### <span data-ttu-id="6a156-131">Boole</span><span class="sxs-lookup"><span data-stu-id="6a156-131">Boolean</span></span>

## <span data-ttu-id="6a156-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6a156-132">NOTES</span></span>

## <span data-ttu-id="6a156-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6a156-133">RELATED LINKS</span></span>

[<span data-ttu-id="6a156-134">Get-Azurermapımanagementsubscription</span><span class="sxs-lookup"><span data-stu-id="6a156-134">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="6a156-135">Yeni-Azurermapımanagementsubscription</span><span class="sxs-lookup"><span data-stu-id="6a156-135">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="6a156-136">Set-Azurermapımanagementsubscription</span><span class="sxs-lookup"><span data-stu-id="6a156-136">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)

