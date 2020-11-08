---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: EC6AB7E9-BC9F-4FA2-8172-144C9842D74C
online version: ''
schema: 2.0.0
ms.openlocfilehash: da7ed2c382bfcec8327b291c46a51699b77b9373
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105630"
---
# <span data-ttu-id="17fa5-101">Get-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="17fa5-101">Get-AzureRemoteAppVmStaleAdObject</span></span>

## <span data-ttu-id="17fa5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17fa5-102">SYNOPSIS</span></span>
<span data-ttu-id="17fa5-103">Azure Active Directory 'de, artık varolmayan Azure RemoteApp sanal makinelerle ilişkili nesneleri alır.</span><span class="sxs-lookup"><span data-stu-id="17fa5-103">Gets objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>

## <span data-ttu-id="17fa5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="17fa5-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="17fa5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="17fa5-105">DESCRIPTION</span></span>
<span data-ttu-id="17fa5-106">**Get-Azureremoteappvmetradobject** cmdlet 'ı Azure Active Directory 'de, artık varolmayan Azure RemoteApp sanal makinelerle ilişkili nesneleri alır.</span><span class="sxs-lookup"><span data-stu-id="17fa5-106">The **Get-AzureRemoteAppVmStaleAdObject** cmdlet gets objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>
<span data-ttu-id="17fa5-107">Bu cmdlet, aldığı her nesnenin adını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="17fa5-107">This cmdlet displays the name of each object that it gets.</span></span>

## <span data-ttu-id="17fa5-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="17fa5-108">EXAMPLES</span></span>

### <span data-ttu-id="17fa5-109">Örnek 1: koleksiyon için eski nesneleri alma</span><span class="sxs-lookup"><span data-stu-id="17fa5-109">Example 1: Get stale objects for a collection</span></span>
```
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso"
```

<span data-ttu-id="17fa5-110">Bu ikinci komut contoso adlı koleksiyonun eski nesnelerini alır.</span><span class="sxs-lookup"><span data-stu-id="17fa5-110">This second command gets the stale objects for the collection named Contoso.</span></span>

## <span data-ttu-id="17fa5-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="17fa5-111">PARAMETERS</span></span>

### <span data-ttu-id="17fa5-112">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="17fa5-112">-CollectionName</span></span>
<span data-ttu-id="17fa5-113">Azure RemoteApp koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17fa5-113">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17fa5-114">-Credential</span><span class="sxs-lookup"><span data-stu-id="17fa5-114">-Credential</span></span>
<span data-ttu-id="17fa5-115">Bu eylemi gerçekleştirme hakkına sahip bir kimlik bilgisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="17fa5-115">Specifies a credential that has rights to perform this action.</span></span>
<span data-ttu-id="17fa5-116">**PSCredential** nesnesi almak için **Get-Credential** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="17fa5-116">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="17fa5-117">Bu parametreyi belirtmezseniz, bu cmdlet geçerli kullanıcı kimlik bilgilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="17fa5-117">If you do not specify this parameter, this cmdlet uses the current user credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17fa5-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="17fa5-118">-Profile</span></span>
<span data-ttu-id="17fa5-119">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="17fa5-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="17fa5-120">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="17fa5-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="17fa5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17fa5-121">CommonParameters</span></span>
<span data-ttu-id="17fa5-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="17fa5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17fa5-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17fa5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17fa5-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="17fa5-124">INPUTS</span></span>

## <span data-ttu-id="17fa5-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="17fa5-125">OUTPUTS</span></span>

### <span data-ttu-id="17fa5-126">Dizisi</span><span class="sxs-lookup"><span data-stu-id="17fa5-126">String</span></span>

## <span data-ttu-id="17fa5-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="17fa5-127">NOTES</span></span>

## <span data-ttu-id="17fa5-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="17fa5-128">RELATED LINKS</span></span>

[<span data-ttu-id="17fa5-129">Temizle-Azureremoteappvmeleadobject</span><span class="sxs-lookup"><span data-stu-id="17fa5-129">Clear-AzureRemoteAppVmStaleAdObject</span></span>](./Clear-AzureRemoteAppVmStaleAdObject.md)


