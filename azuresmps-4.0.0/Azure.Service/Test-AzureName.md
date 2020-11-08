---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0DF54C9D-7A19-4591-A1FC-33C6A4C9BF33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 05a99e1a4965329c0eeb29fe0e014814fd1807b2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105937"
---
# <span data-ttu-id="88a15-101">Test-AzureName</span><span class="sxs-lookup"><span data-stu-id="88a15-101">Test-AzureName</span></span>

## <span data-ttu-id="88a15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88a15-102">SYNOPSIS</span></span>
<span data-ttu-id="88a15-103">Microsoft Azure bulut hizmeti adı, depolama hizmeti adı veya hizmet veri yolu ad alanı adı olup olmadığını sınar.</span><span class="sxs-lookup"><span data-stu-id="88a15-103">Tests whether a Microsoft Azure cloud service name, storage service name or service bus namespace name exists or not.</span></span>

## <span data-ttu-id="88a15-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="88a15-104">SYNTAX</span></span>

### <span data-ttu-id="88a15-105">Hizmetinin</span><span class="sxs-lookup"><span data-stu-id="88a15-105">Service</span></span>
```
Test-AzureName [-Service] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="88a15-106">Alanını</span><span class="sxs-lookup"><span data-stu-id="88a15-106">Storage</span></span>
```
Test-AzureName [-Storage] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="88a15-107">ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="88a15-107">ServiceBusNamespace</span></span>
```
Test-AzureName [-ServiceBusNamespace] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="88a15-108">Web sitesi</span><span class="sxs-lookup"><span data-stu-id="88a15-108">Website</span></span>
```
Test-AzureName [-Website] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="88a15-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="88a15-109">DESCRIPTION</span></span>
<span data-ttu-id="88a15-110">Ad varsa, cmdlet $True döndürür.</span><span class="sxs-lookup"><span data-stu-id="88a15-110">If the name exists, the cmdlet returns $True.</span></span>
<span data-ttu-id="88a15-111">Ad yoksa $False döndürür.</span><span class="sxs-lookup"><span data-stu-id="88a15-111">If the name does not exist, it returns $False.</span></span>

## <span data-ttu-id="88a15-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="88a15-112">EXAMPLES</span></span>

### <span data-ttu-id="88a15-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="88a15-113">Example 1</span></span>
```
PS C:\> Test-AzureName -Service "MyNameService1"
```

<span data-ttu-id="88a15-114">Bu komut, "MyNameService1" nin varolan bir Microsoft Azure bulut hizmeti adı olup olmadığını sınar.</span><span class="sxs-lookup"><span data-stu-id="88a15-114">This command tests to see if the "MyNameService1" is an existing Microsoft Azure cloud service name.</span></span>

### <span data-ttu-id="88a15-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="88a15-115">Example 2</span></span>
```
PS C:\> Test-AzureName -Storage "mystorename1"
```

<span data-ttu-id="88a15-116">Bu komut, "mystorename1" nin varolan bir Microsoft Azure depolama hizmeti adı olup olmadığını sınar.</span><span class="sxs-lookup"><span data-stu-id="88a15-116">This command tests to see if the "mystorename1" is an existing Microsoft Azure storage service name.</span></span>

### <span data-ttu-id="88a15-117">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="88a15-117">Example 3</span></span>
```
PS C:\> Test-AzureName -ServiceBusNamespace "mynamespace"
```

<span data-ttu-id="88a15-118">Bu komut, "MyNameSpace" nin varolan bir Microsoft Azure Service Bus ad alanı adı olup olmadığını sınar.</span><span class="sxs-lookup"><span data-stu-id="88a15-118">This command tests to see if the "mynamespace" is an existing Microsoft Azure service bus namespace name.</span></span>

## <span data-ttu-id="88a15-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="88a15-119">PARAMETERS</span></span>

### <span data-ttu-id="88a15-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="88a15-120">-Name</span></span>
<span data-ttu-id="88a15-121">Sınanacak hizmetin adını veya depolama hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="88a15-121">Specifies the name of the service or storage account to test.</span></span>

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

### <span data-ttu-id="88a15-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="88a15-122">-Profile</span></span>
<span data-ttu-id="88a15-123">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="88a15-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="88a15-124">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="88a15-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="88a15-125">-Hizmet</span><span class="sxs-lookup"><span data-stu-id="88a15-125">-Service</span></span>
<span data-ttu-id="88a15-126">Var olan hizmet hesabını sınaytkullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="88a15-126">Specifies to test for an existing service account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a15-127">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="88a15-127">-ServiceBusNamespace</span></span>
<span data-ttu-id="88a15-128">Var olan bir hizmet veri yolu ad boşluğunu sınamanızı belirtir.</span><span class="sxs-lookup"><span data-stu-id="88a15-128">Specifies to test for an existing service bus namespace.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ServiceBusNamespace
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a15-129">-Depolama</span><span class="sxs-lookup"><span data-stu-id="88a15-129">-Storage</span></span>
<span data-ttu-id="88a15-130">Var olan bir depolama hesabını sınaykullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="88a15-130">Specifies to test for an existing storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Storage
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a15-131">-Web sitesi</span><span class="sxs-lookup"><span data-stu-id="88a15-131">-Website</span></span>
<span data-ttu-id="88a15-132">Var olan bir Web sitesinin test edileceği belirtir.</span><span class="sxs-lookup"><span data-stu-id="88a15-132">Specifies to test for an existing website.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Website
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a15-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88a15-133">CommonParameters</span></span>
<span data-ttu-id="88a15-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="88a15-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88a15-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88a15-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88a15-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="88a15-136">INPUTS</span></span>

## <span data-ttu-id="88a15-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="88a15-137">OUTPUTS</span></span>

## <span data-ttu-id="88a15-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="88a15-138">NOTES</span></span>
* <span data-ttu-id="88a15-139">düğüm-dev, php-dev, Python-dev</span><span class="sxs-lookup"><span data-stu-id="88a15-139">node-dev, php-dev, python-dev</span></span>

## <span data-ttu-id="88a15-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="88a15-140">RELATED LINKS</span></span>

