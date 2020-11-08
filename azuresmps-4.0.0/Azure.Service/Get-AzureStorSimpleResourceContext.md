---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7CB42968-8F6F-4D84-9AE2-1000F280BF3C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 586abbd5f203ce00f6faa7975d9e2adbd0c7940e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106549"
---
# <span data-ttu-id="122f3-101">Get-AzureStorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="122f3-101">Get-AzureStorSimpleResourceContext</span></span>

## <span data-ttu-id="122f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="122f3-102">SYNOPSIS</span></span>
<span data-ttu-id="122f3-103">Geçerli kaynak bağlamını alır.</span><span class="sxs-lookup"><span data-stu-id="122f3-103">Gets the current resource context.</span></span>

## <span data-ttu-id="122f3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="122f3-104">SYNTAX</span></span>

```
Get-AzureStorSimpleResourceContext [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="122f3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="122f3-105">DESCRIPTION</span></span>
<span data-ttu-id="122f3-106">**Get-AzureStorSimpleResourceContext** cmdlet 'i geçerli kaynak bağlamını alır.</span><span class="sxs-lookup"><span data-stu-id="122f3-106">The **Get-AzureStorSimpleResourceContext** cmdlet gets the current resource context.</span></span>

## <span data-ttu-id="122f3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="122f3-107">EXAMPLES</span></span>

### <span data-ttu-id="122f3-108">Örnek 1: geçerli bağlamı alma</span><span class="sxs-lookup"><span data-stu-id="122f3-108">Example 1: Get the current context</span></span>
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa" 
PS C:\> Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso63-Tsqa
```

<span data-ttu-id="122f3-109">İlk komut, **Select-AzureStorSimpleResource** cmdlet 'ini kullanarak geçerli içeriği Contoso63-Tsqa adlı kaynak olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="122f3-109">The first command sets the current context to be the resource named Contoso63-Tsqa by using the **Select-AzureStorSimpleResource** cmdlet.</span></span>

<span data-ttu-id="122f3-110">İkinci komut geçerli kaynak bağlamını alır.</span><span class="sxs-lookup"><span data-stu-id="122f3-110">The second command gets the current resource context.</span></span>

### <span data-ttu-id="122f3-111">Örnek 2: geçerli bağlamı edinme girişimi</span><span class="sxs-lookup"><span data-stu-id="122f3-111">Example 2: Attempt to get the current context</span></span>
```
PS C:\>Get-AzureStorSimpleResourceContext
Get-AzureStorSimpleResourceContext : Resource Context is not set for your subscription. Please use
Select-AzureStorSimpleResource -ResourceName <<name>> to set
```

<span data-ttu-id="122f3-112">Bu komut geçerli içeriği alır.</span><span class="sxs-lookup"><span data-stu-id="122f3-112">This command gets the current context.</span></span>
<span data-ttu-id="122f3-113">Bu örnekte, hiçbir bağlam ayarlanmadı.</span><span class="sxs-lookup"><span data-stu-id="122f3-113">In this example, no context has been set.</span></span>
<span data-ttu-id="122f3-114">Komut, sorunu açıklayan bir ileti döndürür.</span><span class="sxs-lookup"><span data-stu-id="122f3-114">The command returns a message that explains the problem.</span></span>

## <span data-ttu-id="122f3-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="122f3-115">PARAMETERS</span></span>

### <span data-ttu-id="122f3-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="122f3-116">-Profile</span></span>
<span data-ttu-id="122f3-117">Bir Azure profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="122f3-117">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="122f3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="122f3-118">CommonParameters</span></span>
<span data-ttu-id="122f3-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="122f3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="122f3-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="122f3-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="122f3-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="122f3-121">INPUTS</span></span>

### <span data-ttu-id="122f3-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="122f3-122">None</span></span>

## <span data-ttu-id="122f3-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="122f3-123">OUTPUTS</span></span>

### <span data-ttu-id="122f3-124">StorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="122f3-124">StorSimpleResourceContext</span></span>
<span data-ttu-id="122f3-125">Bu cmdlet, bir **ResourceContext** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="122f3-125">This cmdlet returns a **ResourceContext** object.</span></span>

## <span data-ttu-id="122f3-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="122f3-126">NOTES</span></span>

## <span data-ttu-id="122f3-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="122f3-127">RELATED LINKS</span></span>

[<span data-ttu-id="122f3-128">Get-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="122f3-128">Get-AzureStorSimpleResource</span></span>](./Get-AzureStorSimpleResource.md)

[<span data-ttu-id="122f3-129">Select-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="122f3-129">Select-AzureStorSimpleResource</span></span>](./Select-AzureStorSimpleResource.md)


