---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4A920D84-0005-45A2-8229-FD9436A2CA6D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 927520466299776326229976b355444f9db6c23e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106049"
---
# <span data-ttu-id="cc7d4-101">Set-AzureService</span><span class="sxs-lookup"><span data-stu-id="cc7d4-101">Set-AzureService</span></span>

## <span data-ttu-id="cc7d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc7d4-102">SYNOPSIS</span></span>
<span data-ttu-id="cc7d4-103">Belirtilen Microsoft Azure hizmetinin etiketini ve açıklamasını ayarlar veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="cc7d4-103">Sets or updates the label and description of the specified Microsoft Azure service.</span></span>

## <span data-ttu-id="cc7d4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cc7d4-104">SYNTAX</span></span>

```
Set-AzureService [-ServiceName] <String> [[-Label] <String>] [[-Description] <String>]
 [[-ReverseDnsFqdn] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="cc7d4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cc7d4-105">DESCRIPTION</span></span>
<span data-ttu-id="cc7d4-106">**Set-AzureService** cmdlet 'i geçerli abonelikteki bir hizmete etiket ve açıklama atar.</span><span class="sxs-lookup"><span data-stu-id="cc7d4-106">The **Set-AzureService** cmdlet assigns a label and description to a service in the current subscription.</span></span>

## <span data-ttu-id="cc7d4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cc7d4-107">EXAMPLES</span></span>

### <span data-ttu-id="cc7d4-108">Örnek 1: hizmetin etiketini ve açıklamasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="cc7d4-108">Example 1: Update the label and description for a service</span></span>
```
PS C:\> C:\PS>Set-AzureService -ServiceName "MySvc1" -Label "MyTestSvc1" -Description "My service for testing out new configurations"
```

<span data-ttu-id="cc7d4-109">Bu komut, MyTestSvc1 hizmeti için etiketi "MyTestSvc1" ve "yeni yapılandırmalar test etmek için hizmetim" olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="cc7d4-109">This command sets the label to "MyTestSvc1" and the description to "My service for testing out new configurations" for the MyTestSvc1 service.</span></span>

## <span data-ttu-id="cc7d4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cc7d4-110">PARAMETERS</span></span>

### <span data-ttu-id="cc7d4-111">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="cc7d4-111">-Description</span></span>
<span data-ttu-id="cc7d4-112">Azure hizmeti için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc7d4-112">Specifies a description for the Azure service.</span></span>
<span data-ttu-id="cc7d4-113">Açıklama en çok 1024 karakter uzunluğunda olabilir.</span><span class="sxs-lookup"><span data-stu-id="cc7d4-113">The description may be up to 1024 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc7d4-114">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="cc7d4-114">-InformationAction</span></span>
<span data-ttu-id="cc7d4-115">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc7d4-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="cc7d4-116">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="cc7d4-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cc7d4-117">'A</span><span class="sxs-lookup"><span data-stu-id="cc7d4-117">Continue</span></span>
- <span data-ttu-id="cc7d4-118">Manıza</span><span class="sxs-lookup"><span data-stu-id="cc7d4-118">Ignore</span></span>
- <span data-ttu-id="cc7d4-119">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="cc7d4-119">Inquire</span></span>
- <span data-ttu-id="cc7d4-120">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="cc7d4-120">SilentlyContinue</span></span>
- <span data-ttu-id="cc7d4-121">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="cc7d4-121">Stop</span></span>
- <span data-ttu-id="cc7d4-122">Biliriz</span><span class="sxs-lookup"><span data-stu-id="cc7d4-122">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc7d4-123">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="cc7d4-123">-InformationVariable</span></span>
<span data-ttu-id="cc7d4-124">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc7d4-124">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc7d4-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="cc7d4-125">-Label</span></span>
<span data-ttu-id="cc7d4-126">Azure hizmeti için bir etiket belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc7d4-126">Specifies a label for the Azure service.</span></span>
<span data-ttu-id="cc7d4-127">Etiket en çok 100 karakter uzunluğunda olabilir.</span><span class="sxs-lookup"><span data-stu-id="cc7d4-127">The label may be up to 100 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc7d4-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="cc7d4-128">-Profile</span></span>
<span data-ttu-id="cc7d4-129">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc7d4-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cc7d4-130">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="cc7d4-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cc7d4-131">-Smardnsfqdn</span><span class="sxs-lookup"><span data-stu-id="cc7d4-131">-ReverseDnsFqdn</span></span>
<span data-ttu-id="cc7d4-132">Geriye doğru DNS için tam nitelikli etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc7d4-132">Specifies the fully qualified domain name for reverse DNS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc7d4-133">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="cc7d4-133">-ServiceName</span></span>
<span data-ttu-id="cc7d4-134">Güncelleştirilecek Azure hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc7d4-134">Specifies the name of the Azure service to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc7d4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc7d4-135">CommonParameters</span></span>
<span data-ttu-id="cc7d4-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cc7d4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc7d4-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc7d4-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc7d4-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cc7d4-138">INPUTS</span></span>

## <span data-ttu-id="cc7d4-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cc7d4-139">OUTPUTS</span></span>

### <span data-ttu-id="cc7d4-140">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="cc7d4-140">ManagementOperationContext</span></span>

## <span data-ttu-id="cc7d4-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cc7d4-141">NOTES</span></span>

## <span data-ttu-id="cc7d4-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cc7d4-142">RELATED LINKS</span></span>

[<span data-ttu-id="cc7d4-143">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="cc7d4-143">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="cc7d4-144">New-AzureService</span><span class="sxs-lookup"><span data-stu-id="cc7d4-144">New-AzureService</span></span>](./New-AzureService.md)


