---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 482E8CD6-C38F-4BD5-8214-016D0D8C7FD0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6381b8e0fac5ebf047122f131af6087d5bb5a9fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105554"
---
# <span data-ttu-id="8169a-101">Get-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="8169a-101">Get-AzureStorSimpleResource</span></span>

## <span data-ttu-id="8169a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8169a-102">SYNOPSIS</span></span>
<span data-ttu-id="8169a-103">Oluşturduğunuz tüm kaynakları alır.</span><span class="sxs-lookup"><span data-stu-id="8169a-103">Gets all resources that you created.</span></span>

## <span data-ttu-id="8169a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8169a-104">SYNTAX</span></span>

```
Get-AzureStorSimpleResource [-ResourceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8169a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8169a-105">DESCRIPTION</span></span>
<span data-ttu-id="8169a-106">**Get-AzureStorSimpleResource** cmdlet 'ı, Azure Portal kullanarak oluşturduğunuz tüm kaynakları alır.</span><span class="sxs-lookup"><span data-stu-id="8169a-106">The **Get-AzureStorSimpleResource** cmdlet gets all resources that you created by using Azure Portal.</span></span>
<span data-ttu-id="8169a-107">Cmdlet, kaynaklara bağlanmak için kullanabileceğiniz ayrıntıları alır.</span><span class="sxs-lookup"><span data-stu-id="8169a-107">The cmdlet gets details you can use to connect to the resources.</span></span>

## <span data-ttu-id="8169a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8169a-108">EXAMPLES</span></span>

### <span data-ttu-id="8169a-109">Örnek 1: tüm kaynakları alma</span><span class="sxs-lookup"><span data-stu-id="8169a-109">Example 1: Get all resources</span></span>
```
PS C:\>Get-AzureStorSimpleResource
VERBOSE: ClientRequestId: 5cd61b91-ef40-43b4-986d-156e06d2ed65_PS

ResourceName                                      ResourceId           ResourceState
------------                                      ----------           -------------
Contoso63-Tsqa                                    8838459798595306468  Started
Contoso68-Tsqa                                    2859070203638134681  Started
Contoso73-Tsqa                                    7871392677286863733  Started
Contoso87-Tsqa                                    1909806764156522689  Started
VERBOSE: Found 4 StorSimple resources.
```

<span data-ttu-id="8169a-110">Bu komut, oluşturduğunuz tüm kaynakları alır.</span><span class="sxs-lookup"><span data-stu-id="8169a-110">This command gets all the resources you created.</span></span>
<span data-ttu-id="8169a-111">Bu örnekte üç kaynak vardır.</span><span class="sxs-lookup"><span data-stu-id="8169a-111">In this example, there are three resources.</span></span>

### <span data-ttu-id="8169a-112">Örnek 2: adını kullanarak bir kaynak alma</span><span class="sxs-lookup"><span data-stu-id="8169a-112">Example 2: Get a resource by using its name</span></span>
```
PS C:\>Get-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa"
VERBOSE: ClientRequestId: efc3c85c-12aa-4345-b6eb-ccc532de4825_PS

ResourceName                                      ResourceId           ResourceState
------------                                      ----------           -------------
Contoso63-Tsqa                                    1909806764156522689  Started
VERBOSE: Found 1 StorSimple resource.
```

<span data-ttu-id="8169a-113">Bu komut, Contoso63-Tsqa adlı kaynağı alır.</span><span class="sxs-lookup"><span data-stu-id="8169a-113">This command gets the resource named Contoso63-Tsqa.</span></span>

### <span data-ttu-id="8169a-114">Örnek 3: varolmayan bir kaynağı edinme girişimi</span><span class="sxs-lookup"><span data-stu-id="8169a-114">Example 3: Attempt to get a nonexistent resource</span></span>
```
PS C:\>Get-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa"
VERBOSE: ClientRequestId: 5d08d40b-f9d7-4d43-956f-13f01e89625b_PS
VERBOSE: Invalid input : Could not find a resource named Contoso64-Tsqa in your subscription.
```

<span data-ttu-id="8169a-115">Bu komut, Contoso64-Tsqa adlı kaynağı almayı dener.</span><span class="sxs-lookup"><span data-stu-id="8169a-115">This command attempts to get the resource named Contoso64-Tsqa.</span></span>
<span data-ttu-id="8169a-116">Bu ada sahip bir kaynak yok.</span><span class="sxs-lookup"><span data-stu-id="8169a-116">There is no resource that has this name.</span></span>
<span data-ttu-id="8169a-117">Bu örnek herhangi bir kaynak döndürmez.</span><span class="sxs-lookup"><span data-stu-id="8169a-117">This example does not return any resource.</span></span>

## <span data-ttu-id="8169a-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8169a-118">PARAMETERS</span></span>

### <span data-ttu-id="8169a-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="8169a-119">-Profile</span></span>
<span data-ttu-id="8169a-120">Bir Azure profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="8169a-120">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8169a-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8169a-121">-ResourceName</span></span>
<span data-ttu-id="8169a-122">Bu cmdlet 'in aldığı kaynağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8169a-122">Specifies the name of the resource that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8169a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8169a-123">CommonParameters</span></span>
<span data-ttu-id="8169a-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8169a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8169a-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8169a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8169a-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8169a-126">INPUTS</span></span>

### <span data-ttu-id="8169a-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8169a-127">None</span></span>

## <span data-ttu-id="8169a-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8169a-128">OUTPUTS</span></span>

### <span data-ttu-id="8169a-129">IEnumerable \<ResourceCredentials\> , ResourceCredentials</span><span class="sxs-lookup"><span data-stu-id="8169a-129">IEnumerable\<ResourceCredentials\>, ResourceCredentials</span></span>
<span data-ttu-id="8169a-130">Bu cmdlet, aşağıdaki özellikleri içeren **ResourceCredentials** nesnelerini döndürür:</span><span class="sxs-lookup"><span data-stu-id="8169a-130">This cmdlet returns **ResourceCredentials** objects that contain the following properties:</span></span> 

- <span data-ttu-id="8169a-131">**Kaynak**</span><span class="sxs-lookup"><span data-stu-id="8169a-131">**ResourceName**</span></span>
- <span data-ttu-id="8169a-132">**Kaynak kimliği**</span><span class="sxs-lookup"><span data-stu-id="8169a-132">**ResouceId**</span></span>
- <span data-ttu-id="8169a-133">**ResourceState**</span><span class="sxs-lookup"><span data-stu-id="8169a-133">**ResourceState**</span></span>

## <span data-ttu-id="8169a-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8169a-134">NOTES</span></span>

## <span data-ttu-id="8169a-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8169a-135">RELATED LINKS</span></span>

[<span data-ttu-id="8169a-136">Get-AzureStorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="8169a-136">Get-AzureStorSimpleResourceContext</span></span>](./Get-AzureStorSimpleResourceContext.md)

[<span data-ttu-id="8169a-137">Select-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="8169a-137">Select-AzureStorSimpleResource</span></span>](./Select-AzureStorSimpleResource.md)


