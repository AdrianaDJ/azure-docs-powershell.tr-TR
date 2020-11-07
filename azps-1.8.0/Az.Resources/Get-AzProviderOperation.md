---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: bd0483cf03ac5cff224824cc41b3fab994006acb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759427"
---
# <span data-ttu-id="b6b94-101">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="b6b94-101">Get-AzProviderOperation</span></span>

## <span data-ttu-id="b6b94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6b94-102">SYNOPSIS</span></span>
<span data-ttu-id="b6b94-103">Azure RBAC kullanarak güvenliği sağlanabilir bir Azure Kaynak sağlayıcısı için işlemleri alır.</span><span class="sxs-lookup"><span data-stu-id="b6b94-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

## <span data-ttu-id="b6b94-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b6b94-104">SYNTAX</span></span>

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6b94-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b6b94-105">DESCRIPTION</span></span>
<span data-ttu-id="b6b94-106">Get-AzProviderOperation, Azure kaynak sağlayıcıları tarafından sağlanan işlemleri alır.</span><span class="sxs-lookup"><span data-stu-id="b6b94-106">The Get-AzProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="b6b94-107">İşlemler Azure RBAC 'de özel roller oluşturmaya eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="b6b94-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="b6b94-108">Bu komut, görüntülenecek işlem ayrıntılarını belirleyen bir işlem arama dizesi (joker karakter () içeren) olarak alır *. Tüm Azure Resource providers için tüm işlemleri almak için Get-AzProviderOperation \* kullanın. Microsoft. COMPUTE/' Get-AzProviderOperation kullanarak* Microsoft 'un tüm işlemlerini alın. kaynak sağlayıcısını hesaplama.</span><span class="sxs-lookup"><span data-stu-id="b6b94-108">The command takes as input an operation search string (with possible wildcard( *) character(s)) which determines the operations details to display. Use Get-AzProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="b6b94-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b6b94-109">EXAMPLES</span></span>

### <span data-ttu-id="b6b94-110">Tüm sağlayıcılar için tüm eylemleri alma</span><span class="sxs-lookup"><span data-stu-id="b6b94-110">Get all actions for all providers</span></span>
```
PS C:\> Get-AzProviderOperation *
```

### <span data-ttu-id="b6b94-111">Belirli bir kaynak sağlayıcısının eylemlerini alma</span><span class="sxs-lookup"><span data-stu-id="b6b94-111">Get actions for a particular resource provider</span></span>
```
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="b6b94-112">Sanal makinelerde gerçekleştirilebilen tüm eylemleri alma</span><span class="sxs-lookup"><span data-stu-id="b6b94-112">Get all actions that can be performed on virtual machines</span></span>
```
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## <span data-ttu-id="b6b94-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b6b94-113">PARAMETERS</span></span>

### <span data-ttu-id="b6b94-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6b94-114">-DefaultProfile</span></span>
<span data-ttu-id="b6b94-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b6b94-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6b94-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="b6b94-116">-OperationSearchString</span></span>
<span data-ttu-id="b6b94-117">İşlem arama dizesi (olası joker karakter (\*) ile)</span><span class="sxs-lookup"><span data-stu-id="b6b94-117">The operation search string (with possible wildcard (\*) characters)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: "*"
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6b94-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6b94-118">CommonParameters</span></span>
<span data-ttu-id="b6b94-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b6b94-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6b94-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6b94-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6b94-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b6b94-121">INPUTS</span></span>

### <span data-ttu-id="b6b94-122">System. String</span><span class="sxs-lookup"><span data-stu-id="b6b94-122">System.String</span></span>

## <span data-ttu-id="b6b94-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b6b94-123">OUTPUTS</span></span>

### <span data-ttu-id="b6b94-124">Microsoft. Azure. Commands. resources. modeller. PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="b6b94-124">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="b6b94-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b6b94-125">NOTES</span></span>
<span data-ttu-id="b6b94-126">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="b6b94-126">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="b6b94-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b6b94-127">RELATED LINKS</span></span>
