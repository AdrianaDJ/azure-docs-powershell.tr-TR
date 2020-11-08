---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 71302FB6-7E2B-4972-A743-AB537AC7CD79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79e194e0f8dda4392dec191881702c680bf172ac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106552"
---
# <span data-ttu-id="37189-101">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="37189-101">Get-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="37189-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37189-102">SYNOPSIS</span></span>
<span data-ttu-id="37189-103">Hizmet yapılandırmasındaki erişim denetimi kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="37189-103">Gets access control records in a service configuration.</span></span>

## <span data-ttu-id="37189-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="37189-104">SYNTAX</span></span>

```
Get-AzureStorSimpleAccessControlRecord [-ACRName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="37189-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="37189-105">DESCRIPTION</span></span>
<span data-ttu-id="37189-106">**Get-AzureStorSimpleAccessControlRecord** cmdlet 'ı StorSimple Manager hizmet yapılandırmasındaki erişim denetimi kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="37189-106">The **Get-AzureStorSimpleAccessControlRecord** cmdlet gets access control records in the StorSimple Manager service configuration.</span></span>
<span data-ttu-id="37189-107">Bu cmdlet tüm kayıtları veya adlandırılmış kaydı alır.</span><span class="sxs-lookup"><span data-stu-id="37189-107">This cmdlet gets all records or a named record.</span></span>

<span data-ttu-id="37189-108">Access denetim kayıtları, Iscsı başlatıcı parametrelerinin kapsayıcılarıdır.</span><span class="sxs-lookup"><span data-stu-id="37189-108">Access control records are containers of iSCSI initiator parameters.</span></span>
<span data-ttu-id="37189-109">Bu parametreler hangi başlatıcıların birime erişebileceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="37189-109">These parameters specify which initiators can access a volume.</span></span>
<span data-ttu-id="37189-110">Bir Iscsı başlatıcısı bir birime bağlanmaya çalıştığında, bu birime atanmış erişim denetimi kayıtlarını kontrol eder.</span><span class="sxs-lookup"><span data-stu-id="37189-110">When an iSCSI initiator attempts to connect to a volume, your appliance checks the access control records assigned to that volume.</span></span>
<span data-ttu-id="37189-111">Iscsı başlatıcı parametreleri, bu birimle eşlenmiş bir erişim denetimi kaydındaki girdilerden biriyle eşleşirse, Iscsı Başlatıcısı bağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="37189-111">If the iSCSI initiator parameters match one of the entries in an access control record mapped to that volume, the iSCSI initiator can connect.</span></span>

## <span data-ttu-id="37189-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="37189-112">EXAMPLES</span></span>

### <span data-ttu-id="37189-113">Örnek 1: tüm erişim denetimi kayıtlarını alma</span><span class="sxs-lookup"><span data-stu-id="37189-113">Example 1: Get all access control records</span></span>
```
PS C:\>Get-AzureStorSimpleAccessControlRecord
InstanceId                           Name                        InitiatorName               VolumeCount
----------                           ----                        -------------               -----------
01a31aa5-14de-4b77-b926-2842577f540e Windows_XYUSFL718-RV_ACR    iqn.1991-05.com.microsof... 3
071c282d-0cd2-4c5f-b687-48966037ba48 Linux_XYUSFL719_ACR         iqn.1994-05.com.redhat:a... 3
4600eade-71f8-4d04-baec-0e7cf1d1e8fb Windows_XYUSFL720_ACR       iqn.1991-05.com.microsof... 9
d508d6f0-fcda-4624-b223-c0b307d6113e Linux_XYUSFL350_ACR         iqn.1991-05.com.microsof... 9
```

<span data-ttu-id="37189-114">Bu komut, tüm erişim denetimi kayıtlarını alır.</span><span class="sxs-lookup"><span data-stu-id="37189-114">This command gets all access control records.</span></span>

### <span data-ttu-id="37189-115">Örnek 2: belirli bir erişim denetimi kaydı alma</span><span class="sxs-lookup"><span data-stu-id="37189-115">Example 2: Get a specific access control record</span></span>
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr11"
VERBOSE: ClientRequestId: 61f261c7-acd3-4bcc-922a-ddfd85eb767b_PS
VERBOSE: ClientRequestId: 49c6a4c7-d299-46fd-a553-034c52b47487_PS

GlobalId            : 
InitiatorName       : iqn-contoso63
InstanceId          : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
Name                : Acr11
OperationInProgress : None
VolumeCount         : 6

VERBOSE: Access Control Record with given name Acr11 is found!
```

<span data-ttu-id="37189-116">Bu komut, Acr11 adlı erişim denetimi kaydını alır.</span><span class="sxs-lookup"><span data-stu-id="37189-116">This command gets the access control record named Acr11.</span></span>

## <span data-ttu-id="37189-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="37189-117">PARAMETERS</span></span>

### <span data-ttu-id="37189-118">-ACRName</span><span class="sxs-lookup"><span data-stu-id="37189-118">-ACRName</span></span>
<span data-ttu-id="37189-119">Alınacak bir erişim denetimi kaydının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="37189-119">Specifies the name of an access control record to get.</span></span>

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

### <span data-ttu-id="37189-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="37189-120">-Profile</span></span>
<span data-ttu-id="37189-121">Bir Azure profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="37189-121">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="37189-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37189-122">CommonParameters</span></span>
<span data-ttu-id="37189-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="37189-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37189-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37189-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37189-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="37189-125">INPUTS</span></span>

### <span data-ttu-id="37189-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="37189-126">None</span></span>

## <span data-ttu-id="37189-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="37189-127">OUTPUTS</span></span>

### <span data-ttu-id="37189-128">AccessControlRecord, IList\<AccessControlRecord\></span><span class="sxs-lookup"><span data-stu-id="37189-128">AccessControlRecord, IList\<AccessControlRecord\></span></span>
<span data-ttu-id="37189-129">Bu cmdlet bir **Accesscontrolrecord** nesnesi veya **\<AccessControlRecord\> IList** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="37189-129">This cmdlet returns an **AccessControlRecord** object or an **IList\<AccessControlRecord\>** object.</span></span>
<span data-ttu-id="37189-130">**Accesscontrolrecord** nesnesi aşağıdaki alanları içerir:</span><span class="sxs-lookup"><span data-stu-id="37189-130">An **AccessControlRecord** object contains the following fields:</span></span> 

- <span data-ttu-id="37189-131">**Globalid** ( **dize** )</span><span class="sxs-lookup"><span data-stu-id="37189-131">**GlobalId** ( **String** )</span></span> 
- <span data-ttu-id="37189-132">**Initiatorname** ( **dize** )</span><span class="sxs-lookup"><span data-stu-id="37189-132">**InitiatorName** ( **String** )</span></span> 
- <span data-ttu-id="37189-133">**InstanceId** ( **dize** )</span><span class="sxs-lookup"><span data-stu-id="37189-133">**InstanceId** ( **String** )</span></span> 
- <span data-ttu-id="37189-134">**Ad** ( **dize** )</span><span class="sxs-lookup"><span data-stu-id="37189-134">**Name** ( **String** )</span></span> 
- <span data-ttu-id="37189-135">**Operationınprogress** ( **operationınprogress** )</span><span class="sxs-lookup"><span data-stu-id="37189-135">**OperationInProgress** ( **OperationInProgress** )</span></span> 
- <span data-ttu-id="37189-136">**Birimsayısı** ( **int** )</span><span class="sxs-lookup"><span data-stu-id="37189-136">**VolumeCount** ( **int** )</span></span>

## <span data-ttu-id="37189-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="37189-137">NOTES</span></span>

## <span data-ttu-id="37189-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="37189-138">RELATED LINKS</span></span>

[<span data-ttu-id="37189-139">New-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="37189-139">New-AzureStorSimpleAccessControlRecord</span></span>](./New-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="37189-140">Remove-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="37189-140">Remove-AzureStorSimpleAccessControlRecord</span></span>](./Remove-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="37189-141">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="37189-141">Set-AzureStorSimpleAccessControlRecord</span></span>](./Set-AzureStorSimpleAccessControlRecord.md)


