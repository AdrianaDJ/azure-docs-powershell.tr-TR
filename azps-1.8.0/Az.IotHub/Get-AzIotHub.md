---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
ms.openlocfilehash: d544de6badaa6ce64e8165696cc7dff2a595d75e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916484"
---
# <span data-ttu-id="a9435-101">Get-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="a9435-101">Get-AzIotHub</span></span>

## <span data-ttu-id="a9435-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9435-102">SYNOPSIS</span></span>
<span data-ttu-id="a9435-103">Bir abonelikteki ıothubs hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="a9435-103">Gets information about the IotHubs in a subscription.</span></span>

## <span data-ttu-id="a9435-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a9435-104">SYNTAX</span></span>

### <span data-ttu-id="a9435-105">ListIotHubsByResourceGroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a9435-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9435-106">Getilebilirlik Ubbyname</span><span class="sxs-lookup"><span data-stu-id="a9435-106">GetIotHubByName</span></span>
```
Get-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9435-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9435-107">DESCRIPTION</span></span>
<span data-ttu-id="a9435-108">Bir abonelikteki ıothubs hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="a9435-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="a9435-109">Bir abonelikteki tüm IotHub örneklerini görüntüleyebilir ya da sonuçlarınızı kaynak grubuna veya belirli bir IotHub adına göre filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a9435-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="a9435-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a9435-110">EXAMPLES</span></span>

### <span data-ttu-id="a9435-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a9435-111">Example 1</span></span>
```
PS C:\> Get-AzIotHub
```

<span data-ttu-id="a9435-112">Abonelikteki tüm ıothubleri alır.</span><span class="sxs-lookup"><span data-stu-id="a9435-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="a9435-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a9435-113">Example 2</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="a9435-114">Aboneliğindeki tüm ıothubleri "myresourcegroup" adlı resourcegroup 'a ait olarak alır.</span><span class="sxs-lookup"><span data-stu-id="a9435-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="a9435-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="a9435-115">Example 3</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="a9435-116">"Myiothub" adındaki IotHub hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="a9435-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="a9435-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a9435-117">PARAMETERS</span></span>

### <span data-ttu-id="a9435-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9435-118">-DefaultProfile</span></span>
<span data-ttu-id="a9435-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a9435-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9435-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="a9435-120">-Name</span></span>
<span data-ttu-id="a9435-121">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="a9435-121">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9435-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9435-122">-ResourceGroupName</span></span>
<span data-ttu-id="a9435-123">ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a9435-123">Name of the ResourceGroup</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotHubsByResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9435-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9435-124">CommonParameters</span></span>
<span data-ttu-id="a9435-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a9435-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9435-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9435-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9435-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a9435-127">INPUTS</span></span>

### <span data-ttu-id="a9435-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a9435-128">System.String</span></span>

## <span data-ttu-id="a9435-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a9435-129">OUTPUTS</span></span>

### <span data-ttu-id="a9435-130">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="a9435-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="a9435-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a9435-131">NOTES</span></span>

## <span data-ttu-id="a9435-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a9435-132">RELATED LINKS</span></span>
