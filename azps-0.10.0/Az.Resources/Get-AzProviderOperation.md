---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: 21e1af2a36478f2e0b8e470660d0fbe2539a396e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936437"
---
# <span data-ttu-id="398a6-101">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="398a6-101">Get-AzProviderOperation</span></span>

## <span data-ttu-id="398a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="398a6-102">SYNOPSIS</span></span>
<span data-ttu-id="398a6-103">Azure RBAC kullanarak güvenliği sağlanabilir bir Azure Kaynak sağlayıcısı için işlemleri alır.</span><span class="sxs-lookup"><span data-stu-id="398a6-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

## <span data-ttu-id="398a6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="398a6-104">SYNTAX</span></span>

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="398a6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="398a6-105">DESCRIPTION</span></span>
<span data-ttu-id="398a6-106">Get-AzProviderOperation, Azure kaynak sağlayıcıları tarafından sağlanan işlemleri alır.</span><span class="sxs-lookup"><span data-stu-id="398a6-106">The Get-AzProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="398a6-107">İşlemler Azure RBAC 'de özel roller oluşturmaya eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="398a6-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="398a6-108">Bu komut, görüntülenecek işlem ayrıntılarını belirleyen bir işlem arama dizesi (joker karakter () içeren) olarak alır *. Tüm Azure Resource providers için tüm işlemleri almak için Get-AzProviderOperation \* kullanın. Microsoft. COMPUTE/' Get-AzProviderOperation kullanarak* Microsoft 'un tüm işlemlerini alın. kaynak sağlayıcısını hesaplama.</span><span class="sxs-lookup"><span data-stu-id="398a6-108">The command takes as input an operation search string (with possible wildcard( *) character(s)) which determines the operations details to display. Use Get-AzProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="398a6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="398a6-109">EXAMPLES</span></span>

### <span data-ttu-id="398a6-110">Tüm sağlayıcılar için tüm eylemleri alma</span><span class="sxs-lookup"><span data-stu-id="398a6-110">Get all actions for all providers</span></span>
```
PS C:\> Get-AzProviderOperation *
```

### <span data-ttu-id="398a6-111">Belirli bir kaynak sağlayıcısının eylemlerini alma</span><span class="sxs-lookup"><span data-stu-id="398a6-111">Get actions for a particular resource provider</span></span>
```
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="398a6-112">Sanal makinelerde gerçekleştirilebilen tüm eylemleri alma</span><span class="sxs-lookup"><span data-stu-id="398a6-112">Get all actions that can be performed on virtual machines</span></span>
```
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## <span data-ttu-id="398a6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="398a6-113">PARAMETERS</span></span>

### <span data-ttu-id="398a6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="398a6-114">-DefaultProfile</span></span>
<span data-ttu-id="398a6-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="398a6-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="398a6-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="398a6-116">-OperationSearchString</span></span>
<span data-ttu-id="398a6-117">İşlem arama dizesi (olası joker karakter (\*) ile)</span><span class="sxs-lookup"><span data-stu-id="398a6-117">The operation search string (with possible wildcard (\*) characters)</span></span>

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

### <span data-ttu-id="398a6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="398a6-118">CommonParameters</span></span>
<span data-ttu-id="398a6-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="398a6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="398a6-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="398a6-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="398a6-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="398a6-121">INPUTS</span></span>

### <span data-ttu-id="398a6-122">System. String</span><span class="sxs-lookup"><span data-stu-id="398a6-122">System.String</span></span>
<span data-ttu-id="398a6-123">Parametreler: Işlemkimliği (ByValue)</span><span class="sxs-lookup"><span data-stu-id="398a6-123">Parameters: OperationSearchString (ByValue)</span></span>

## <span data-ttu-id="398a6-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="398a6-124">OUTPUTS</span></span>

### <span data-ttu-id="398a6-125">Microsoft. Azure. Commands. resources. modeller. PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="398a6-125">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="398a6-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="398a6-126">NOTES</span></span>
<span data-ttu-id="398a6-127">Anahtar sözcükler: Azure, az, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım</span><span class="sxs-lookup"><span data-stu-id="398a6-127">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="398a6-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="398a6-128">RELATED LINKS</span></span>
