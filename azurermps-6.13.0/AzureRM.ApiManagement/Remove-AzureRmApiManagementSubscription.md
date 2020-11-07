---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 09a0af4685701de60fc85c1572b492e7582ff71e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763506"
---
# <span data-ttu-id="23fda-101">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="23fda-101">Remove-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="23fda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23fda-102">SYNOPSIS</span></span>
<span data-ttu-id="23fda-103">Var olan bir aboneliği siler.</span><span class="sxs-lookup"><span data-stu-id="23fda-103">Deletes an existing subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23fda-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="23fda-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23fda-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="23fda-105">DESCRIPTION</span></span>
<span data-ttu-id="23fda-106">**Remove-Azurermapsananagementsubscription** cmdlet 'i var olan bir aboneliği siler.</span><span class="sxs-lookup"><span data-stu-id="23fda-106">The **Remove-AzureRmApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="23fda-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="23fda-107">EXAMPLES</span></span>

### <span data-ttu-id="23fda-108">Örnek 1: aboneliği silme</span><span class="sxs-lookup"><span data-stu-id="23fda-108">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="23fda-109">Bu komut, var olan bir aboneliği siler.</span><span class="sxs-lookup"><span data-stu-id="23fda-109">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="23fda-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="23fda-110">PARAMETERS</span></span>

### <span data-ttu-id="23fda-111">-Context</span><span class="sxs-lookup"><span data-stu-id="23fda-111">-Context</span></span>
<span data-ttu-id="23fda-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="23fda-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="23fda-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23fda-113">-DefaultProfile</span></span>
<span data-ttu-id="23fda-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="23fda-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23fda-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="23fda-115">-PassThru</span></span>
<span data-ttu-id="23fda-116">Bu cmdlet 'in bir $True değerini (başarılı olursa), aksi takdirde $false değerini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="23fda-116">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="23fda-117">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="23fda-117">-SubscriptionId</span></span>
<span data-ttu-id="23fda-118">Abonelik KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="23fda-118">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="23fda-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="23fda-119">-Confirm</span></span>
<span data-ttu-id="23fda-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="23fda-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23fda-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23fda-121">-WhatIf</span></span>
<span data-ttu-id="23fda-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="23fda-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23fda-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="23fda-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23fda-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23fda-124">CommonParameters</span></span>
<span data-ttu-id="23fda-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="23fda-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23fda-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23fda-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23fda-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="23fda-127">INPUTS</span></span>

### <span data-ttu-id="23fda-128">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="23fda-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="23fda-129">System. String</span><span class="sxs-lookup"><span data-stu-id="23fda-129">System.String</span></span>

### <span data-ttu-id="23fda-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="23fda-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="23fda-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="23fda-131">OUTPUTS</span></span>

### <span data-ttu-id="23fda-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="23fda-132">System.Boolean</span></span>

## <span data-ttu-id="23fda-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="23fda-133">NOTES</span></span>

## <span data-ttu-id="23fda-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="23fda-134">RELATED LINKS</span></span>

[<span data-ttu-id="23fda-135">Get-Azurermapımanagementsubscription</span><span class="sxs-lookup"><span data-stu-id="23fda-135">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="23fda-136">Yeni-Azurermapımanagementsubscription</span><span class="sxs-lookup"><span data-stu-id="23fda-136">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="23fda-137">Set-Azurermapımanagementsubscription</span><span class="sxs-lookup"><span data-stu-id="23fda-137">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


