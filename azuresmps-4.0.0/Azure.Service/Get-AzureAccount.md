---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 70ADAF16-BC52-47BF-A85A-A84DEACDA027
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2704dbdc308b9773452b05ceba24719f2e274132
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105676"
---
# <span data-ttu-id="d5892-101">Get-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="d5892-101">Get-AzureAccount</span></span>

## <span data-ttu-id="d5892-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5892-102">SYNOPSIS</span></span>
<span data-ttu-id="d5892-103">Azure PowerShell tarafından sağlanan Azure hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="d5892-103">Gets Azure accounts that are available to Azure PowerShell.</span></span>

## <span data-ttu-id="d5892-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d5892-104">SYNTAX</span></span>

```
Get-AzureAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d5892-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d5892-105">DESCRIPTION</span></span>
<span data-ttu-id="d5892-106">**Get-AzureAccount** cmdlet 'ı Windows PowerShell tarafından sağlanan Azure hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="d5892-106">The **Get-AzureAccount** cmdlet gets the Azure accounts that are available to Windows PowerShell.</span></span>
<span data-ttu-id="d5892-107">Hesaplarınızı Windows PowerShell 'in kullanımına sunmak için **Add-AzureAccount** veya **Import-publishsettingsfıle** cmdlet 'lerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d5892-107">To make your accounts available to Windows PowerShell, use the **Add-AzureAccount** or **Import-PublishSettingsFile** cmdlets.</span></span>

## <span data-ttu-id="d5892-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d5892-108">EXAMPLES</span></span>

### <span data-ttu-id="d5892-109">Örnek 1: tüm hesapları alma</span><span class="sxs-lookup"><span data-stu-id="d5892-109">Example 1: Get all accounts</span></span>
```
PS C:\> Get-AzureAccount

Name                         ActiveDirectories
----                         -----------------
contosoadmin@outlook.com     {{ ActiveDirectoryTenantId = abcde5cd-bcc3-441a-bd86-e6a...
contosotest1@outlook.com     {{ ActiveDirectoryTenantId = aaeabcde-386c-4466-bf70-794...
```

<span data-ttu-id="d5892-110">Bu komut belirtilen kullanıcıyla ilişkili tüm hesapları alır.</span><span class="sxs-lookup"><span data-stu-id="d5892-110">This command gets all accounts associated with the specified user.</span></span>

### <span data-ttu-id="d5892-111">Örnek 2: ada göre bir hesap alma</span><span class="sxs-lookup"><span data-stu-id="d5892-111">Example 2: Get an account by name</span></span>
```
PS C:\> Get-AzureAccount -Name contosoadmin@outlook.com

Name                         ActiveDirectories
----                         -----------------
contosoadmin@outlook.com     {{ ActiveDirectoryTenantId = abcde5cd-bcc3-441a-bd86-e6a...
```

<span data-ttu-id="d5892-112">Bu komut, ContosoAdmin hesabını alır.</span><span class="sxs-lookup"><span data-stu-id="d5892-112">This command gets the ContosoAdmin account.</span></span>

## <span data-ttu-id="d5892-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d5892-113">PARAMETERS</span></span>

### <span data-ttu-id="d5892-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="d5892-114">-Name</span></span>
<span data-ttu-id="d5892-115">Yalnızca belirtilen hesabı alır.</span><span class="sxs-lookup"><span data-stu-id="d5892-115">Gets only the specified account.</span></span>
<span data-ttu-id="d5892-116">Varsayılan, Windows PowerShell 'in kullanabildiği tüm hesaplardır.</span><span class="sxs-lookup"><span data-stu-id="d5892-116">The default is all accounts that are available to Windows PowerShell.</span></span>
<span data-ttu-id="d5892-117">Hesap adını girin.</span><span class="sxs-lookup"><span data-stu-id="d5892-117">Enter the account name.</span></span>
<span data-ttu-id="d5892-118">**Ad** büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="d5892-118">The **Name** value is case-sensitive.</span></span>
<span data-ttu-id="d5892-119">Joker karakterlere izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="d5892-119">Wildcards are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5892-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="d5892-120">-Profile</span></span>
<span data-ttu-id="d5892-121">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5892-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d5892-122">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="d5892-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d5892-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5892-123">CommonParameters</span></span>
<span data-ttu-id="d5892-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d5892-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5892-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5892-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5892-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d5892-126">INPUTS</span></span>

### <span data-ttu-id="d5892-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d5892-127">None</span></span>
<span data-ttu-id="d5892-128">Bu cmdlet 'e giriş kanalı oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="d5892-128">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="d5892-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d5892-129">OUTPUTS</span></span>

### <span data-ttu-id="d5892-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d5892-130">None</span></span>
<span data-ttu-id="d5892-131">Bu cmdlet hiçbir çıkış döndürmez.</span><span class="sxs-lookup"><span data-stu-id="d5892-131">This cmdlet does not return any output.</span></span>

## <span data-ttu-id="d5892-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d5892-132">NOTES</span></span>

## <span data-ttu-id="d5892-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d5892-133">RELATED LINKS</span></span>

[<span data-ttu-id="d5892-134">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="d5892-134">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="d5892-135">Get-Azuikinci dosyayı</span><span class="sxs-lookup"><span data-stu-id="d5892-135">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)

[<span data-ttu-id="d5892-136">Import-Azuyeniden yayımlayan ayarları dosyası</span><span class="sxs-lookup"><span data-stu-id="d5892-136">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="d5892-137">Remove-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="d5892-137">Remove-AzureAccount</span></span>](./Remove-AzureAccount.md)


