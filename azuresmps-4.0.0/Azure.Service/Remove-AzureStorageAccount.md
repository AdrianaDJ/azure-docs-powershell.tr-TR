---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 679452A6-A6CA-4DC8-8E00-09E369505319
online version: ''
schema: 2.0.0
ms.openlocfilehash: 933c6de8e7baa55b2093a7ffc4ac28fede13bb5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106458"
---
# <span data-ttu-id="201d0-101">Remove-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="201d0-101">Remove-AzureStorageAccount</span></span>

## <span data-ttu-id="201d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="201d0-102">SYNOPSIS</span></span>
<span data-ttu-id="201d0-103">Belirtilen depolama hesabını abonelikten siler.</span><span class="sxs-lookup"><span data-stu-id="201d0-103">Deletes the specified storage account from a subscription.</span></span>

## <span data-ttu-id="201d0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="201d0-104">SYNTAX</span></span>

```
Remove-AzureStorageAccount [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="201d0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="201d0-105">DESCRIPTION</span></span>
<span data-ttu-id="201d0-106">**Remove-AzureStorageAccount** cmdlet 'ı bir Azure aboneliğindeki hesabı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="201d0-106">The **Remove-AzureStorageAccount** cmdlet removes an account from an Azure subscription.</span></span>

## <span data-ttu-id="201d0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="201d0-107">EXAMPLES</span></span>

### <span data-ttu-id="201d0-108">Örnek 1: depolama hesabını kaldırma</span><span class="sxs-lookup"><span data-stu-id="201d0-108">Example 1: Remove a storage account</span></span>
```
PS C:\> Remove-AzureStorageAccount -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="201d0-109">Bu komut, ContosoStore01 depolama hesabını belirtilen abonelikten kaldırır.</span><span class="sxs-lookup"><span data-stu-id="201d0-109">This command removes the ContosoStore01 storage account from the specified subscription.</span></span>

## <span data-ttu-id="201d0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="201d0-110">PARAMETERS</span></span>

### <span data-ttu-id="201d0-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="201d0-111">-InformationAction</span></span>
<span data-ttu-id="201d0-112">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="201d0-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="201d0-113">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="201d0-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="201d0-114">'A</span><span class="sxs-lookup"><span data-stu-id="201d0-114">Continue</span></span>
- <span data-ttu-id="201d0-115">Manıza</span><span class="sxs-lookup"><span data-stu-id="201d0-115">Ignore</span></span>
- <span data-ttu-id="201d0-116">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="201d0-116">Inquire</span></span>
- <span data-ttu-id="201d0-117">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="201d0-117">SilentlyContinue</span></span>
- <span data-ttu-id="201d0-118">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="201d0-118">Stop</span></span>
- <span data-ttu-id="201d0-119">Biliriz</span><span class="sxs-lookup"><span data-stu-id="201d0-119">Suspend</span></span>

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

### <span data-ttu-id="201d0-120">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="201d0-120">-InformationVariable</span></span>
<span data-ttu-id="201d0-121">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="201d0-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="201d0-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="201d0-122">-Profile</span></span>
<span data-ttu-id="201d0-123">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="201d0-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="201d0-124">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="201d0-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="201d0-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="201d0-125">-StorageAccountName</span></span>
<span data-ttu-id="201d0-126">Kaldırılacak depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="201d0-126">Specifies the name of the storage account to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="201d0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="201d0-127">CommonParameters</span></span>
<span data-ttu-id="201d0-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="201d0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="201d0-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="201d0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="201d0-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="201d0-130">INPUTS</span></span>

## <span data-ttu-id="201d0-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="201d0-131">OUTPUTS</span></span>

## <span data-ttu-id="201d0-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="201d0-132">NOTES</span></span>

## <span data-ttu-id="201d0-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="201d0-133">RELATED LINKS</span></span>

[<span data-ttu-id="201d0-134">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="201d0-134">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="201d0-135">Yeni-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="201d0-135">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="201d0-136">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="201d0-136">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


