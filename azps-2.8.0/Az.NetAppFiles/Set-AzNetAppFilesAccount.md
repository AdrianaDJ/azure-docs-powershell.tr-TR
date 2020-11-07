---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
ms.openlocfilehash: 873b506ea1fd50e2869a19a45a302c5fe12a781b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932129"
---
# <span data-ttu-id="a07e9-101">Set-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="a07e9-101">Set-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="a07e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a07e9-102">SYNOPSIS</span></span>
<span data-ttu-id="a07e9-103">Yeni veri kümesiyle Azure NetApp dosyaları (ANF) hesabını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a07e9-103">Updates an Azure NetApp Files (ANF) account with the new data set.</span></span> <span data-ttu-id="a07e9-104">İlişkili etkin dizinlerin silinmesi için kullanışlıdır.</span><span class="sxs-lookup"><span data-stu-id="a07e9-104">Useful for deletion of associated active directories.</span></span>

## <span data-ttu-id="a07e9-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a07e9-105">SYNTAX</span></span>

```
Set-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectories <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a07e9-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="a07e9-106">DESCRIPTION</span></span>
<span data-ttu-id="a07e9-107">**Set-AzNetAppFilesAccount** cmdlet 'i ANF hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a07e9-107">The **Set-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="a07e9-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a07e9-108">EXAMPLES</span></span>

### <span data-ttu-id="a07e9-109">Örnek 1: ANF hesabını değiştirme</span><span class="sxs-lookup"><span data-stu-id="a07e9-109">Example 1 : Modify an ANF account</span></span>
```
PS C:\>Set-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="a07e9-110">Bu komut, verilen hesapta bir güncelleştirme gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="a07e9-110">This command performs an update on the given account.</span></span> <span data-ttu-id="a07e9-111">Active Directory 'nin yokluğu, hesaptan çıkarılacaktır.</span><span class="sxs-lookup"><span data-stu-id="a07e9-111">The absence of the active directory means it will be removed from the account.</span></span>

## <span data-ttu-id="a07e9-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a07e9-112">PARAMETERS</span></span>

### <span data-ttu-id="a07e9-113">-Activedizinler</span><span class="sxs-lookup"><span data-stu-id="a07e9-113">-ActiveDirectories</span></span>
<span data-ttu-id="a07e9-114">Active Directory 'yi temsil eden bir Hashtable dizisi</span><span class="sxs-lookup"><span data-stu-id="a07e9-114">A hashtable array which represents the active directories</span></span>

```yaml
Type: PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a07e9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a07e9-115">-DefaultProfile</span></span>
<span data-ttu-id="a07e9-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a07e9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a07e9-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="a07e9-117">-Location</span></span>
<span data-ttu-id="a07e9-118">Kaynağın konumu</span><span class="sxs-lookup"><span data-stu-id="a07e9-118">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a07e9-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="a07e9-119">-Name</span></span>
<span data-ttu-id="a07e9-120">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="a07e9-120">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a07e9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a07e9-121">-ResourceGroupName</span></span>
<span data-ttu-id="a07e9-122">ANF hesabının kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="a07e9-122">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a07e9-123">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a07e9-123">-Tag</span></span>
<span data-ttu-id="a07e9-124">Kaynak etiketlerini temsil eden bir Hashtable</span><span class="sxs-lookup"><span data-stu-id="a07e9-124">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a07e9-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="a07e9-125">-Confirm</span></span>
<span data-ttu-id="a07e9-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a07e9-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a07e9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a07e9-127">-WhatIf</span></span>
<span data-ttu-id="a07e9-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a07e9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a07e9-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a07e9-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a07e9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a07e9-130">CommonParameters</span></span>
<span data-ttu-id="a07e9-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a07e9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a07e9-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a07e9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a07e9-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a07e9-133">INPUTS</span></span>

### <span data-ttu-id="a07e9-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a07e9-134">None</span></span>

## <span data-ttu-id="a07e9-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a07e9-135">OUTPUTS</span></span>

### <span data-ttu-id="a07e9-136">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="a07e9-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="a07e9-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a07e9-137">NOTES</span></span>

## <span data-ttu-id="a07e9-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a07e9-138">RELATED LINKS</span></span>
