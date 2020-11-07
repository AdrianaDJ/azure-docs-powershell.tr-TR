---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
ms.openlocfilehash: 51229c966c0e4c8b0ec74c3c940037aca5081b15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764008"
---
# <span data-ttu-id="f7f0d-101">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="f7f0d-101">Get-AzureRmProviderOperation</span></span>

## <span data-ttu-id="f7f0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7f0d-102">SYNOPSIS</span></span>
<span data-ttu-id="f7f0d-103">Azure RBAC kullanarak güvenliği sağlanabilir bir Azure Kaynak sağlayıcısı için işlemleri alır.</span><span class="sxs-lookup"><span data-stu-id="f7f0d-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7f0d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f7f0d-104">SYNTAX</span></span>

```
Get-AzureRmProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7f0d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f7f0d-105">DESCRIPTION</span></span>
<span data-ttu-id="f7f0d-106">Get-AzureRmProviderOperation, Azure kaynak sağlayıcıları tarafından sağlanan işlemleri alır.</span><span class="sxs-lookup"><span data-stu-id="f7f0d-106">The Get-AzureRmProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="f7f0d-107">İşlemler Azure RBAC 'de özel roller oluşturmaya eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="f7f0d-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="f7f0d-108">Bu komut, görüntülenecek işlem ayrıntılarını belirleyen bir işlem arama dizesi (*) karakteri ((*) karakteri) olarak alır.</span><span class="sxs-lookup"><span data-stu-id="f7f0d-108">The command takes as input an operation search string (with possible wildcard(\*) character(s)) which determines the operations details to display.</span></span>

<span data-ttu-id="f7f0d-109">Tüm Azure Resource providers için tüm işlemleri almak için Get-AzureRmProviderOperation \* kullanın.</span><span class="sxs-lookup"><span data-stu-id="f7f0d-109">Use Get-AzureRmProviderOperation \* to get all operations for all Azure resource providers.</span></span>

<span data-ttu-id="f7f0d-110">Microsoft 'un tüm işlemlerini almak için Microsoft. COMPUTE/\* Get-AzureRmProviderOperation kullanın. kaynak sağlayıcısını hesaplama.</span><span class="sxs-lookup"><span data-stu-id="f7f0d-110">Use Get-AzureRmProviderOperation Microsoft.Compute/\* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="f7f0d-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f7f0d-111">EXAMPLES</span></span>

### <span data-ttu-id="f7f0d-112">Tüm sağlayıcılar için tüm eylemleri alma</span><span class="sxs-lookup"><span data-stu-id="f7f0d-112">Get all actions for all providers</span></span>
```
PS C:\> Get-AzureRmProviderOperation *
```

### <span data-ttu-id="f7f0d-113">Belirli bir kaynak sağlayıcısının eylemlerini alma</span><span class="sxs-lookup"><span data-stu-id="f7f0d-113">Get actions for a particular resource provider</span></span>
```
PS C:\> Get-AzureRmProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="f7f0d-114">Sanal makinelerde gerçekleştirilebilen tüm eylemleri alma</span><span class="sxs-lookup"><span data-stu-id="f7f0d-114">Get all actions that can be performed on virtual machines</span></span>
```
PS C:\> Get-AzureRmProviderOperation */virtualMachines/*
```

## <span data-ttu-id="f7f0d-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f7f0d-115">PARAMETERS</span></span>

### <span data-ttu-id="f7f0d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7f0d-116">-DefaultProfile</span></span>
<span data-ttu-id="f7f0d-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f7f0d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7f0d-118">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="f7f0d-118">-OperationSearchString</span></span>
<span data-ttu-id="f7f0d-119">İşlem arama dizesi (olası joker karakter (\*) ile)</span><span class="sxs-lookup"><span data-stu-id="f7f0d-119">The operation search string (with possible wildcard (\*) characters)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: "*"
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7f0d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7f0d-120">CommonParameters</span></span>
<span data-ttu-id="f7f0d-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f7f0d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7f0d-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7f0d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7f0d-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f7f0d-123">INPUTS</span></span>

### <span data-ttu-id="f7f0d-124">Dizisi</span><span class="sxs-lookup"><span data-stu-id="f7f0d-124">String</span></span>
<span data-ttu-id="f7f0d-125">' OperationSearchString ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="f7f0d-125">Parameter 'OperationSearchString' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="f7f0d-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f7f0d-126">OUTPUTS</span></span>

### <span data-ttu-id="f7f0d-127">Microsoft. Azure. Commands. resources. modeller. PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="f7f0d-127">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="f7f0d-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f7f0d-128">NOTES</span></span>
<span data-ttu-id="f7f0d-129">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="f7f0d-129">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="f7f0d-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f7f0d-130">RELATED LINKS</span></span>
