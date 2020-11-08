---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
ms.openlocfilehash: ecbf6a847ad208b49e11ab0089f9cf486763ddf3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108957"
---
# <span data-ttu-id="4dd27-101">Set-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="4dd27-101">Set-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="4dd27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dd27-102">SYNOPSIS</span></span>
<span data-ttu-id="4dd27-103">Yeni veri kümesiyle Azure NetApp dosyaları (ANF) hesabını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4dd27-103">Updates an Azure NetApp Files (ANF) account with the new data set.</span></span> <span data-ttu-id="4dd27-104">İlişkili etkin dizinlerin silinmesi için kullanışlıdır.</span><span class="sxs-lookup"><span data-stu-id="4dd27-104">Useful for deletion of associated active directories.</span></span>

## <span data-ttu-id="4dd27-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4dd27-105">SYNTAX</span></span>

### <span data-ttu-id="4dd27-106">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4dd27-106">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dd27-107">SetByResourceActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="4dd27-107">SetByResourceActiveDirectory</span></span>
```
Set-AzNetAppFilesAccount -Location <String> -Name <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dd27-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4dd27-108">DESCRIPTION</span></span>
<span data-ttu-id="4dd27-109">**Set-AzNetAppFilesAccount** cmdlet 'i ANF hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4dd27-109">The **Set-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="4dd27-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4dd27-110">EXAMPLES</span></span>

### <span data-ttu-id="4dd27-111">Örnek 1: ANF hesabını değiştirme</span><span class="sxs-lookup"><span data-stu-id="4dd27-111">Example 1 : Modify an ANF account</span></span>
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

<span data-ttu-id="4dd27-112">Bu komut, verilen hesapta bir güncelleştirme gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="4dd27-112">This command performs an update on the given account.</span></span> <span data-ttu-id="4dd27-113">Active Directory 'nin yokluğu, hesaptan çıkarılacaktır.</span><span class="sxs-lookup"><span data-stu-id="4dd27-113">The absence of the active directory means it will be removed from the account.</span></span>

## <span data-ttu-id="4dd27-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4dd27-114">PARAMETERS</span></span>

### <span data-ttu-id="4dd27-115">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="4dd27-115">-ActiveDirectory</span></span>
<span data-ttu-id="4dd27-116">Active Directory 'yi temsil eden bir Hashtable dizisi</span><span class="sxs-lookup"><span data-stu-id="4dd27-116">A hashtable array which represents the active directories</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory[]
Parameter Sets: SetByResourceActiveDirectory
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dd27-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dd27-117">-DefaultProfile</span></span>
<span data-ttu-id="4dd27-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4dd27-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dd27-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="4dd27-119">-Location</span></span>
<span data-ttu-id="4dd27-120">Kaynağın konumu</span><span class="sxs-lookup"><span data-stu-id="4dd27-120">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dd27-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="4dd27-121">-Name</span></span>
<span data-ttu-id="4dd27-122">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="4dd27-122">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dd27-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dd27-123">-ResourceGroupName</span></span>
<span data-ttu-id="4dd27-124">ANF hesabının kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="4dd27-124">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dd27-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="4dd27-125">-Tag</span></span>
<span data-ttu-id="4dd27-126">Kaynak etiketlerini temsil eden bir Hashtable</span><span class="sxs-lookup"><span data-stu-id="4dd27-126">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dd27-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="4dd27-127">-Confirm</span></span>
<span data-ttu-id="4dd27-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4dd27-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dd27-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dd27-129">-WhatIf</span></span>
<span data-ttu-id="4dd27-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4dd27-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dd27-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4dd27-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dd27-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dd27-132">CommonParameters</span></span>
<span data-ttu-id="4dd27-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4dd27-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dd27-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4dd27-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dd27-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4dd27-135">INPUTS</span></span>

### <span data-ttu-id="4dd27-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4dd27-136">None</span></span>

## <span data-ttu-id="4dd27-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4dd27-137">OUTPUTS</span></span>

### <span data-ttu-id="4dd27-138">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="4dd27-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="4dd27-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4dd27-139">NOTES</span></span>

## <span data-ttu-id="4dd27-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4dd27-140">RELATED LINKS</span></span>
