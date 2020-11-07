---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermprovideroperation
schema: 2.0.0
ms.openlocfilehash: 1274b04ed85917a9c1e185bfbef6307eaedecc05
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939472"
---
# <span data-ttu-id="24378-101">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="24378-101">Get-AzureRmProviderOperation</span></span>

## <span data-ttu-id="24378-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24378-102">SYNOPSIS</span></span>
<span data-ttu-id="24378-103">Azure RBAC kullanarak güvenliği sağlanabilir bir Azure Kaynak sağlayıcısı için işlemleri alır.</span><span class="sxs-lookup"><span data-stu-id="24378-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24378-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="24378-104">SYNTAX</span></span>

```
Get-AzureRmProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="24378-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="24378-105">DESCRIPTION</span></span>
<span data-ttu-id="24378-106">Get-AzureRmProviderOperation, Azure kaynak sağlayıcıları tarafından sağlanan işlemleri alır.</span><span class="sxs-lookup"><span data-stu-id="24378-106">The Get-AzureRmProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="24378-107">İşlemler Azure RBAC 'de özel roller oluşturmaya eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="24378-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="24378-108">Bu komut, görüntülenecek işlem ayrıntılarını belirleyen bir işlem arama dizesi (joker karakter () içeren) olarak alır *. Tüm Azure Resource providers için tüm işlemleri almak için Get-AzureRmProviderOperation \* kullanın. Microsoft. COMPUTE/' Get-AzureRmProviderOperation kullanarak* Microsoft 'un tüm işlemlerini alın. kaynak sağlayıcısını hesaplama.</span><span class="sxs-lookup"><span data-stu-id="24378-108">The command takes as input an operation search string (with possible wildcard( *) character(s)) which determines the operations details to display. Use Get-AzureRmProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzureRmProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="24378-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="24378-109">EXAMPLES</span></span>

### <span data-ttu-id="24378-110">Tüm sağlayıcılar için tüm eylemleri alma</span><span class="sxs-lookup"><span data-stu-id="24378-110">Get all actions for all providers</span></span>
```
PS C:\> Get-AzureRmProviderOperation *
```

### <span data-ttu-id="24378-111">Belirli bir kaynak sağlayıcısının eylemlerini alma</span><span class="sxs-lookup"><span data-stu-id="24378-111">Get actions for a particular resource provider</span></span>
```
PS C:\> Get-AzureRmProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="24378-112">Sanal makinelerde gerçekleştirilebilen tüm eylemleri alma</span><span class="sxs-lookup"><span data-stu-id="24378-112">Get all actions that can be performed on virtual machines</span></span>
```
PS C:\> Get-AzureRmProviderOperation */virtualMachines/*
```

## <span data-ttu-id="24378-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="24378-113">PARAMETERS</span></span>

### <span data-ttu-id="24378-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24378-114">-DefaultProfile</span></span>
<span data-ttu-id="24378-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="24378-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24378-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="24378-116">-OperationSearchString</span></span>
<span data-ttu-id="24378-117">İşlem arama dizesi (olası joker karakter (\*) ile)</span><span class="sxs-lookup"><span data-stu-id="24378-117">The operation search string (with possible wildcard (\*) characters)</span></span>

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

### <span data-ttu-id="24378-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24378-118">CommonParameters</span></span>
<span data-ttu-id="24378-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="24378-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24378-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24378-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24378-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="24378-121">INPUTS</span></span>

### <span data-ttu-id="24378-122">System. String</span><span class="sxs-lookup"><span data-stu-id="24378-122">System.String</span></span>
<span data-ttu-id="24378-123">Parametreler: Işlemkimliği (ByValue)</span><span class="sxs-lookup"><span data-stu-id="24378-123">Parameters: OperationSearchString (ByValue)</span></span>

## <span data-ttu-id="24378-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="24378-124">OUTPUTS</span></span>

### <span data-ttu-id="24378-125">Microsoft. Azure. Commands. resources. modeller. PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="24378-125">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="24378-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="24378-126">NOTES</span></span>
<span data-ttu-id="24378-127">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="24378-127">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="24378-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="24378-128">RELATED LINKS</span></span>
